guard 'livereload' do
  watch 'result.html'
end

guard 'shell' do
  files = 'Rakefile', 'code.coffee'
  watch(/(#{files * ?| })/) { `rake` }
end
