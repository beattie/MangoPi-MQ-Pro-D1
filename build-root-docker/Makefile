image_built:
	docker build -t buildroot:18.04 .
	touch image_built

image_remove:
	docker image rm buildroot:18.04
	rm -f image_built

clean:
	rm -f image_built
