VERSION = 0.8
EXTRA_CFLAGS  = -Wall -g -D_REENTRANT -DVERSION=\"$(VERSION)\"
INCDIR	= -I /home/user/android-ndk-r7b/platforms/android-9/arch-arm/usr/include/
LIBDIR  = /home/user/android-ndk-r7b/platforms/android-9/arch-arm/usr/lib/
LDFLAGS = -L$(LIBDIR) -static
BFLAGS  = -B $(LIBDIR) -B /home/user/android-ndk-r7b/toolchains/arm-linux-androideabi-4.4.3/prebuilt/windows/lib/gcc/arm-linux-androideabi/4.4.3
RM      = rm -f

TRG = incsfree
OBJ = gopt.o incsfree.o 

all: $(OBJ)
	arm-linux-androideabi-gcc -Wall $(INCDIR) $(BFLAGS) -static -o $(TRG) $(OBJ)

%.o: %.c
	arm-linux-androideabi-gcc -Wall $(CFLAGS) $(INCDIR) -static $(BFLAGS) -c $<

clean:
	$(RM) *.o
	$(RM) *.d
	$(RM) incsfree
	
