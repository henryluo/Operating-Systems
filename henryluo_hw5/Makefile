ifneq ($(KERNELRELEASE),)
	obj-m := memory.o 
else
	KERNELDIR :=/lib/modules/$(shell uname -r)/build
	PWD := $(shell pwd)
	ARCH := arm
	CROSS := arm-linux-

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

clean:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) clean

endif