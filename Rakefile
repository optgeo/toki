desc 'install UNVT in Raspbian'
task :world do
  sh 'curl -sL https://unvt.github.io/equinox/install.sh | bash -'
end

desc 'build style.json and validate it'
task :style do
  sh 'parse-hocon hocon/style.conf > docs/style.json'
  sh 'gl-style-validate docs/style.json'
end

desc 'locally host the site'
task :host do
  sh 'budo -d docs'
end

