require 'yaml'

task :default => [:helper]

task :helper do
	`sass --scss --style compact src\\helper.scss dist\\helper.css`
	`sass --scss --style compressed src\\helper.scss dist\\helper.min.css`
	file = File.read('dist\\helper.css')
	file = file.gsub(/\n\n/, "\n")
	file = file.gsub(/\/\* \*\//, "")
	File.open('dist\\helper.css', 'w') do |f|
		f.puts file
	end
	puts 'Build complete'
end
