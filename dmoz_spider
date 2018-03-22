import scrapy

class DmozSpider(scrapy.Spider): 
	name = "dmoz"
	allowed_domains = ["dmoz.org"] 
	start_urls = [
			"http://www.dmoz.org.in/index.php?c=2245", 
			"http://www.dmoz.org.in/index.php?c=2268"
			]

	def parse(self, response):
		filename = response.url.split("/")[-2] + '.html'
		with open(filename, 'wb') as f: 
			f.write(response.body)
