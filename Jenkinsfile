stage 'se441-qotd-pipeline'

node {
	git 'https://github.com/rooneybb/se441-qotd.git'

	def gradleHome = tool 'Gradle-2.11'
	bat "${gradleHome}\\bin\\gradle.bat assemble uploadArchives sonarqube test"

	step([$class: 'ArtifactArchiver', artifacts: '**/*.war', fingerprint: true])
 }