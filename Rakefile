require 'rubygems'
require 'optparse'
require 'yaml'
 
task :np do
  OptionParser.new.parse!
  ARGV.shift
  title = ARGV.join(' ')
 
  path = "_drafts/#{Date.today}-#{title.downcase.gsub(/[^[:alnum:]]+/, '-')}.markdown"
  
  if File.exist?(path)
    puts "[WARN] File exists - skipping create"
  else
    File.open(path, "w") do |file|
      file.puts YAML.dump({'date' => Date.today, 'layout' => 'post', 'published' => true, 
                           'title' => title, 'comments' => true, 'categories' => []})
      file.puts "---"
    end
  end
  `mvim #{path}`
 
  exit 1
end
