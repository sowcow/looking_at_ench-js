require 'slim'
require 'sass'

task default: :make
desc 'compiles stuff'
task :make do
  scope = Object.new
  page = Slim::Template.new { XXX }.render(scope)
  File.write 'result.html', page
end


XXX = <<xxx
doctype 5
html
  head
    title Game
    sass:
      *
        margin:  0
        padding: 0
  body
    script src='js/enchant.js'
    coffee:
      enchant()
      window.onload = ->
        game = new Core 160, 160
        game.preload 'ass/map0.png'
        game.preload 'ass/space3.png'
        game.add = (obj) -> this.rootScene.addChild obj
        game.onload = ->
          tiles = game.assets['ass/map0.png']
          bg = new Sprite(160, 160)
          image = new Surface(160, 160)
          for j in [0..9]
            for i in [0..9]
              x = i * 16
              y = j * 16
              image.draw tiles, 0, 0, 16, 16, x, y, 16, 16
          bg.image = image
          game.add bg

          bear = new Sprite 32, 32
          bear.image = game.assets['ass/space3.png']
          bear.frame = [15,15,16,16,16,16,15,15,17,17,17,17]
          game.add bear
          
        game.start()
xxx
