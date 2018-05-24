import RPi.GPIO as GPIO import timeimport pygame
pygame.mixer.init()

GPIO.setmode(GPIO.BOARD)
GPIO.setup(3,GPIO.IN)
GPIO.setup(7,GPIO.IN)
GPIO.setup(11,GPIO.IN)
GPIO.setup(12,GPIO.IN)
GPIO.setup(13,GPIO.IN)
GPIO.setup(15,GPIO.IN)
GPIO.setup(16,GPIO.IN)
GPIO.setup(18,GPIO.IN)
GPIO.setup(23,GPIO.OUT)

import RPi.GPIO as GPIO import time
import pygame
pygame.mixer.init()

GPIO.setmode(GPIO.BOARD)
GPIO.setup(3,GPIO.IN)
GPIO.setup(7,GPIO.IN)
GPIO.setup(11,GPIO.IN)
GPIO.setup(12,GPIO.IN)
GPIO.setup(13,GPIO.IN)
GPIO.setup(15,GPIO.IN)
GPIO.setup(16,GPIO.IN)
GPIO.setup(18,GPIO.IN)
GPIO.setup(23,GPIO.OUT)
GPIO.output(23,True)

while 1:

	if GPIO.input(3): a0=1
	else:
	a0=0

	if GPIO.input(7): a1=1
	else:	a1=0
		
	if GPIO.input(11): a2=1
	else:	a2=0
		
	if GPIO.input(12): a3=1
	else:	a3=0
	
	if GPIO.input(13): a4=1
	else:	a4=0
	
	if GPIO.input(15): a5=1
	else:	a5=0
	
	if GPIO.input(16): a6=1
	else:	a6=0
		
	if GPIO.input(18): a7=1
	else:	a7=0
		
	x = a1*1 + a2*4 + a2*8 + a3*16 + a4*32 + a5*64 + a6*128 + a7*255if x<42:
	pygame.mixer.music.load("2.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:	
	continue
	
	elif x>42 and x<84:
	pygame.mixer.music.load("1.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:
	continue

	elif x>84 and x<126:
	pygame.mixer.music.load("3rd_String_G_64kb.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:
	continue

	elif x>126 and x<168:
	pygame.mixer.music.load("4th_String_D_64kb.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:	
	continue
	
	elif x>168 and x<210:
	pygame.mixer.music.load("5th_string_A_64kb.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:	
	continue

	elif x>210:
	pygame.mixer.music.load("6th_String_E_64kb.wav")
	pygame.mixer.music.play()
	while pygame.mixer.music.get_busy() == True:	
	continue
