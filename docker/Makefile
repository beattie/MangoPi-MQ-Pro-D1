image_built:
	docker build -t MangoPi-MQ-Pro-D1 .
	touch image_built

image_remove:
	docker image rm MangoPi-MQ-Pro-D1
	rm -f image_built

clean:
	rm -f image_built
