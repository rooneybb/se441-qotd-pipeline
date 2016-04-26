stage "se441-qotd-pipeline"

node {
	git 'https://github.com/rooneybb/se441-qotd-pipeline.git'

	def gradleHome = tool 'gradle-2.11'
	bat "${gradleHome}\\bin\\gradle.bat assemble uploadArchives"

	step([$class: 'ArtifactArchiver', artifacts: '**/*.war', fingerprint: true])
 }