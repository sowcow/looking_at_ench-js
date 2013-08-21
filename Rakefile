require 'slim'
require 'sass'
require 'coffee-script'

task default: :make
desc 'compiles stuff'
task :make do
  scope = Object.new
  page = Slim::Template.new { XXX }.render(scope)
  File.write 'result.html', page
end


#map = <<map
#'''''~~'''
#'''''~~'''
#''''''~~''
#''''''~~~~
#''''''~'~~
#'''''~~'''
#''''~~''''
#''''~'''''
#''''~'''''
#''''~'''''
#map
#map = Map[map]



code = File.read('code.coffee')
#code = map +?\n+ code

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
#{code.indent(+6)}
xxx


BEGIN{
  #class Map
  #  singleton_class.send :alias_method, :[], :new
  #end

  module It
    refine String do
      def indent num
        pre = ' ' * 6
        lines.map { |x| pre + x }.join
      end
    end
  end
  using It
}
