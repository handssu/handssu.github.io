---
layout: page
title: About
permalink: /about/
toc: true
---

## Personality
밝고 긍정적이다. 사람을 좋아하는 성격으로 함께 얘기하며 에너지를 얻는다. 평소에는 감정적이지만 무언가를 판단해야 할 때는 이성적이다. 계획적인 성격으로 평소에 무엇을 해야 할지 계획해서 실행하는 편이며 계획이 틀어졌을 때도 미리 세워둔 다른 계획을 실행하거나 첫번째 계획을 세웠을 때 얻은 정보를 바탕으로 빠르게 두번째 계획을 세워 실행한다.

## My strong point
정보나 규정에 대한 이해도가 높아 적응이 빠르며 새로운 기술을 빠르게 습득하여 활용할 수 있다.

## Goal
정보보안 분야 중 하나를 정해 전문적으로 깊게 배워서 기업에 취직하여 기술을 성장시키면서 사람들의 정보를 지키며 살고 싶다.

## Study records

### METAVERSE
Gathertown - 밀양여자고등학교 2021 온라인 동아리 발표회, 29 October, 2021
Link: [동아리 발표회 게더타운](https://app.gather.town/app/m1IjXwS67BeHLlDV/TG-Technology%20Growth)

ZEP - 밀양여자고등학교 2022 온라인 발표회
Link: [동아리 발표회 ZEP](https://zep.us/play/24JvZV)

### PY_GAME
몽중인 - 2021 동아리 발표회를 위한 밀양여자고등학교 IT 동아리 TG의 프로젝트 결과물
<div>
  <button id="toggle-button1">몽중인 코드</button>
  <pre id="code-block1" style="display: none;">
    <code>
import pygame, sys, random, time
from pygame.locals import *

pygame.init()
screen = pygame.display.set_mode((1200, 700))
clock = pygame.time.Clock()
menu = "home"
font1 = pygame.font.SysFont("malgungothic", 60)
mc_lives = (pygame.image.load("life1.png").convert_alpha(),
            pygame.image.load("life2.png").convert_alpha(),
            pygame.image.load("life3.png").convert_alpha())

home_image = pygame.image.load("home.png").convert()
apilog_image = pygame.image.load("apilog.jpg").convert()
apilog2_image = pygame.image.load("apilog2.jpg").convert()
stage1_image = pygame.image.load("stage1.jpg").convert()
stage1_bed_image = pygame.image.load("stage1_bed.jpg").convert()
stage1_book_image = pygame.image.load("stage1_book.jpg").convert()
stage1_flower_image = pygame.image.load("stage1_flower.jpg").convert()
stage2_image = pygame.image.load("stage2.png").convert()
stage3_image = pygame.image.load("stage3.jpg").convert()
stage3_before_image = pygame.image.load("stage3_before.png").convert()
add_image = pygame.image.load("add.png").convert()
add_bed_image = pygame.image.load("add_bed.png").convert()
add_book_image = pygame.image.load("add_book.png").convert()
add2_image = pygame.image.load("add2.png").convert()
add3_image = pygame.image.load("add3.png").convert()
star_image = pygame.image.load("star.png").convert_alpha()
star1_image = pygame.image.load("star1.png").convert_alpha()
star2_image = pygame.image.load("star2.png").convert_alpha()
star3_image = pygame.image.load("star3.png").convert_alpha()
star4_image = pygame.image.load("star4.png").convert_alpha()
twinkle_star_image = pygame.image.load("twinkle_star.png").convert_alpha()
addone_image = pygame.image.load("1add.png").convert()
addtwo_image = pygame.image.load("2add.png").convert()
addthree_image = pygame.image.load("3add.png").convert()
addfour_image = pygame.image.load("4add.png").convert()
gameover_image = pygame.image.load("gameover.jpg").convert()
finish1_image = pygame.image.load("finish1.jpg").convert()
finish2_image = pygame.image.load("finish2.jpg").convert()
finish3_image = pygame.image.load("finish3.jpg").convert()
fin_image = pygame.image.load("fin.jpg").convert()


class MC:

    def __init__(self):
        self.lives = 3

    def harm(self):
        self.lives -= 1


mc = MC()

while 1:
    clock.tick(30)
    for event in pygame.event.get():
        if event.type == QUIT:
            sys.exit()
    pressed_keys = pygame.key.get_pressed()

    if menu == "home":
        screen.blit(home_image, (0, 0))
        txt100000 = font1.render("START", True, (255, 255, 255))
        buttonrect100000 = pygame.Rect((500, 400), txt100000.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect100000)
        screen.blit(txt100000, (500, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect100000.collidepoint(
                pygame.mouse.get_pos()):
            menu = "apilog"

    if menu == "apilog":
        screen.blit(apilog_image, (0, 0))
        if pressed_keys[K_1]:
            menu = "apilog2"

        txt4444 = font1.render("1을 눌러 계속하기>>", True, (255, 255, 255))
        screen.blit(txt4444, (0, 600))

    if menu == "apilog2":
        screen.blit(apilog2_image, (0, 0))
        if pressed_keys[K_2]:
            menu = "stage1"

        txt4444 = font1.render("2을 눌러 계속하기>>", True, (255, 255, 255))
        screen.blit(txt4444, (0, 600))

    if menu == "stage1":
        screen.blit(stage1_image, (0, 0))
        screen.blit(star1_image, (480, 30))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                480, 30, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "clock"
        screen.blit(star2_image, (200, 600))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                200, 600, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "bed"
        screen.blit(star3_image, (70, 0))
        screen.blit(star4_image, (950, 200))

    if menu == "clock":
        screen.blit(add_image, (0, 0))
        txt1 = font1.render("시침의 위치를 바꿔볼까?", True, (255, 255, 255))
        screen.blit(txt1, (200, 150))

        txt2 = font1.render("YES", True, (255, 255, 255))
        buttonrect2 = pygame.Rect((400, 400), txt2.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect2)
        screen.blit(txt2, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect2.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "stage1"

        txt3 = font1.render("NO", True, (255, 255, 255))
        buttonrect3 = pygame.Rect((700, 400), txt3.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect3)
        screen.blit(txt3, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect3.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1"

    if menu == "bed":
        screen.blit(add_image, (0, 0))
        txt4 = font1.render("이불을 정리할까?", True, (255, 255, 255))
        screen.blit(txt4, (200, 150))

        txt5 = font1.render("YES", True, (255, 255, 255))
        buttonrect5 = pygame.Rect((400, 400), txt5.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect5)
        screen.blit(txt5, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect5.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1_bed"

        txt6 = font1.render("NO", True, (255, 255, 255))
        buttonrect6 = pygame.Rect((700, 400), txt6.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect6)
        screen.blit(txt6, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect6.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1"

    if menu == "stage1_bed":
        screen.blit(stage1_bed_image, (0, 0))
        screen.blit(star3_image, (70, 0))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                70, 0, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "book"
        screen.blit(star4_image, (950, 200))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                950, 200, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "flower"

    if menu == "book":
        screen.blit(add_bed_image, (0, 0))
        txt7 = font1.render("다른 책을 꽂을까?", True, (255, 255, 255))
        screen.blit(txt7, (200, 150))

        txt8 = font1.render("YES", True, (255, 255, 255))
        buttonrect8 = pygame.Rect((400, 400), txt8.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect8)
        screen.blit(txt8, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect8.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1_book"

        txt9 = font1.render("NO", True, (255, 255, 255))
        buttonrect9 = pygame.Rect((700, 400), txt9.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect9)
        screen.blit(txt9, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect9.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1_bed"

    if menu == "stage1_book":
        screen.blit(stage1_book_image, (0, 0))
        screen.blit(star4_image, (950, 200))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                950, 200, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "flower"

    if menu == "flower":
        screen.blit(add_book_image, (0, 0))
        txt10 = font1.render("꽃 하나를 꽂을까?", True, (255, 255, 255))
        screen.blit(txt10, (200, 150))

        txt11 = font1.render("YES", True, (255, 255, 255))
        buttonrect11 = pygame.Rect((400, 400), txt11.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect11)
        screen.blit(txt11, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect11.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage2"

        txt12 = font1.render("NO", True, (255, 255, 255))
        buttonrect12 = pygame.Rect((700, 400), txt12.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect12)
        screen.blit(txt12, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect12.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage1_book"

    if menu == "stage2":
        screen.blit(stage2_image, (0, 0))
        screen.blit(star1_image, (200, 200))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                200, 200, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "lighter"
        screen.blit(star2_image, (300, 600))
        screen.blit(star3_image, (900, 350))
        screen.blit(star4_image, (800, 150))

    if menu == "lighter":
        screen.blit(add2_image, (0, 0))
        txt13 = font1.render("책상 밑을 조사할까?", True, (255, 255, 255))
        screen.blit(txt13, (200, 150))

        txt14 = font1.render("YES", True, (255, 255, 255))
        buttonrect14 = pygame.Rect((400, 400), txt14.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect14)
        screen.blit(txt14, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect14.collidepoint(
                pygame.mouse.get_pos()):
            menu = "lighter_add"

        txt15 = font1.render("NO", True, (255, 255, 255))
        buttonrect15 = pygame.Rect((700, 400), txt15.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect15)
        screen.blit(txt15, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect15.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage2"

    if menu == "lighter_add":
        screen.blit(addone_image, (0, 0))
        screen.blit(star2_image, (300, 600))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                300, 600, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "crown"
        screen.blit(star3_image, (900, 350))
        screen.blit(star4_image, (800, 150))

    if menu == "crown":
        screen.blit(add2_image, (0, 0))
        txt16 = font1.render("카페트 밑을 조사할까?", True, (255, 255, 255))
        screen.blit(txt16, (200, 150))

        txt17 = font1.render("YES", True, (255, 255, 255))
        buttonrect17 = pygame.Rect((400, 400), txt17.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect17)
        screen.blit(txt17, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect17.collidepoint(
                pygame.mouse.get_pos()):
            menu = "crown_add"

        txt18 = font1.render("NO", True, (255, 255, 255))
        buttonrect18 = pygame.Rect((700, 400), txt18.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect18)
        screen.blit(txt18, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect18.collidepoint(
                pygame.mouse.get_pos()):
            menu = "lighter_add"

    if menu == "crown_add":
        screen.blit(addtwo_image, (0, 0))
        screen.blit(star3_image, (900, 350))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                900, 350, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "triangle"
        screen.blit(star4_image, (800, 150))

    if menu == "triangle":
        screen.blit(add2_image, (0, 0))
        txt19 = font1.render("소파를 조사할까?", True, (255, 255, 255))
        screen.blit(txt19, (200, 150))

        txt20 = font1.render("YES", True, (255, 255, 255))
        buttonrect20 = pygame.Rect((400, 400), txt20.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect20)
        screen.blit(txt20, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect20.collidepoint(
                pygame.mouse.get_pos()):
            menu = "triangle_add"

        txt21 = font1.render("NO", True, (255, 255, 255))
        buttonrect21 = pygame.Rect((700, 400), txt21.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect21)
        screen.blit(txt21, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect21.collidepoint(
                pygame.mouse.get_pos()):
            menu = "crown_add"

    if menu == "triangle_add":
        screen.blit(addthree_image, (0, 0))
        screen.blit(star4_image, (800, 150))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                800, 150, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "circle"

    if menu == "circle":
        screen.blit(add2_image, (0, 0))
        txt22 = font1.render("서랍을 조사할까?", True, (255, 255, 255))
        screen.blit(txt22, (200, 150))

        txt23 = font1.render("YES", True, (255, 255, 255))
        buttonrect23 = pygame.Rect((400, 400), txt23.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect23)
        screen.blit(txt23, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect23.collidepoint(
                pygame.mouse.get_pos()):
            menu = "circle_add"

        txt24 = font1.render("NO", True, (255, 255, 255))
        buttonrect24 = pygame.Rect((700, 400), txt24.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect24)
        screen.blit(txt24, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect24.collidepoint(
                pygame.mouse.get_pos()):
            menu = "triangle_add"

    if menu == "circle_add":
        screen.blit(addfour_image, (0, 0))
        screen.blit(star_image, (650, 150))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                650, 150, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "put"

    if menu == "put":
        screen.blit(add2_image, (0, 0))
        txt25 = font1.render("조각들을 끼울까?", True, (255, 255, 255))
        screen.blit(txt25, (200, 150))

        txt26 = font1.render("YES", True, (255, 255, 255))
        buttonrect26 = pygame.Rect((400, 400), txt26.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect26)
        screen.blit(txt26, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect26.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage3_before"

        txt27 = font1.render("NO", True, (255, 255, 255))
        buttonrect27 = pygame.Rect((700, 400), txt27.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect27)
        screen.blit(txt27, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect27.collidepoint(
                pygame.mouse.get_pos()):
            menu = "circle_add"

    if menu == "stage3_before":
        screen.blit(stage3_before_image, (0, 0))
        screen.blit(star_image, (20, 550))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                20, 550, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "stage3_before2"

    if menu == "stage3_before2":
        screen.blit(stage3_before_image, (0, 0))
        txt28 = font1.render("라이터를 사용할까?", True, (255, 255, 255))
        screen.blit(txt28, (200, 150))

        txt29 = font1.render("YES", True, (255, 255, 255))
        buttonrect29 = pygame.Rect((400, 400), txt29.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect29)
        screen.blit(txt29, (400, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect29.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage3"

        txt30 = font1.render("NO", True, (255, 255, 255))
        buttonrect30 = pygame.Rect((700, 400), txt30.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect30)
        screen.blit(txt30, (700, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect30.collidepoint(
                pygame.mouse.get_pos()):
            menu = "stage3_before"

    if menu == "stage3":
        screen.blit(stage3_image, (0, 0))
        screen.blit(twinkle_star_image, (0, 0))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
                0, 0, 100, 100).collidepoint(pygame.mouse.get_pos()):
            menu = "Q1_before"

    if menu == "Q1_before":
        screen.blit(add3_image, (0, 0))
        txt111 = font1.render("마지막 스테이지를", True, (255, 255, 255))
        txt112 = font1.render("시작해 볼까요?", True, (255, 255, 255))
        screen.blit(txt111, (200, 150))
        screen.blit(txt112, (200, 250))

        if pressed_keys[K_3]:
            menu = "Q1"
        txt1111 = font1.render("3을 눌러 계속하기>>", True, (255, 255, 255))
        buttonrect1111 = pygame.Rect((350, 400), txt1111.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect1111)
        screen.blit(txt1111, (350, 400))

    if menu == "Q1":
        screen.blit(add3_image, (0, 0))
        txt31 = font1.render("TG는 무엇의 약자인가요?", True, (255, 255, 255))
        screen.blit(txt31, (150, 50))

        txt32 = font1.render("1. Technology Ggirickggicick", True,
                             (255, 255, 255))
        buttonrect32 = pygame.Rect((200, 150), txt32.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect32)
        screen.blit(txt32, (200, 150))
        if pygame.mouse.get_pressed()[0] and buttonrect32.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q1"
        txt321 = font1.render("(기술로 끼릭끼릭)", True, (255, 255, 255))
        buttonrect321 = pygame.Rect((200, 250), txt321.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect321)
        screen.blit(txt321, (200, 250))
        if pygame.mouse.get_pressed()[0] and buttonrect321.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q1"

        txt33 = font1.render("2. Technology Growth(기술 성장)", True,
                             (255, 255, 255))
        buttonrect33 = pygame.Rect((200, 350), txt33.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect33)
        screen.blit(txt33, (200, 350))
        if pygame.mouse.get_pressed()[0] and buttonrect33.collidepoint(
                pygame.mouse.get_pos()):
            menu = "A1"

        txt34 = font1.render("3. Tell me Gorilla", True, (255, 255, 255))
        buttonrect34 = pygame.Rect((200, 450), txt34.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect34)
        screen.blit(txt34, (200, 450))
        if pygame.mouse.get_pressed()[0] and buttonrect34.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q1"
        txt341 = font1.render("(나한테 말해줘 고릴라야)", True, (255, 255, 255))
        buttonrect341 = pygame.Rect((200, 550), txt341.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect341)
        screen.blit(txt341, (200, 550))
        if pygame.mouse.get_pressed()[0] and buttonrect341.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q1"

    if menu == "A1":
        screen.blit(add3_image, (0, 0))
        txt35 = font1.render("맞습니다! TG는 Technology Growth의", True,
                             (255, 255, 255))
        txt351 = font1.render("약자로 기술을 배움으로써 성장하겠", True, (255, 255, 255))
        txt352 = font1.render("다는 의미로 지었습니다만 사실", True, (255, 255, 255))
        txt353 = font1.render("기술로 끼릭끼릭(Technology Ggirickggrick)", True,
                              (255, 255, 255))
        txt354 = font1.render("하고 싶지만 차마 실천하지 못해서", True, (255, 255, 255))
        txt355 = font1.render("틀어서 지은 이름이랍니다 ㅋㅋㅋ", True, (255, 255, 255))
        screen.blit(txt35, (100, 50))
        screen.blit(txt351, (100, 150))
        screen.blit(txt352, (100, 250))
        screen.blit(txt353, (80, 350))
        screen.blit(txt354, (100, 450))
        screen.blit(txt355, (100, 550))

        if pressed_keys[K_4]:
            menu = "Q2"
        txt11111 = font1.render("4을 눌러 계속하기>>", True, (255, 255, 255))
        buttonrect11111 = pygame.Rect((300, 610), txt11111.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect11111)
        screen.blit(txt11111, (300, 610))

    if menu == "Q2":
        screen.blit(add3_image, (0, 0))
        txt37 = font1.render("TG 동아리와 관련된 계열은?", True, (255, 255, 255))
        screen.blit(txt37, (150, 100))

        txt38 = font1.render("1. 교육계열", True, (255, 255, 255))
        buttonrect38 = pygame.Rect((250, 200), txt38.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect38)
        screen.blit(txt38, (250, 200))
        if pygame.mouse.get_pressed()[0] and buttonrect38.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q2"

        txt39 = font1.render("2. 자연과학계열", True, (255, 255, 255))
        buttonrect39 = pygame.Rect((250, 300), txt39.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect39)
        screen.blit(txt39, (250, 300))
        if pygame.mouse.get_pressed()[0] and buttonrect39.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q2"

        txt40 = font1.render("3. 답뭐계열", True, (255, 255, 255))
        buttonrect40 = pygame.Rect((250, 400), txt40.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect40)
        screen.blit(txt40, (250, 400))
        if pygame.mouse.get_pressed()[0] and buttonrect40.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q2"

        txt41 = font1.render("4. 공학계열", True, (255, 255, 255))
        buttonrect41 = pygame.Rect((250, 500), txt41.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect41)
        screen.blit(txt41, (250, 500))
        if pygame.mouse.get_pressed()[0] and buttonrect41.collidepoint(
                pygame.mouse.get_pos()):
            menu = "A2"

        txt42 = font1.render("5. 예체능계열", True, (255, 255, 255))
        buttonrect42 = pygame.Rect((250, 600), txt42.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect42)
        screen.blit(txt42, (250, 600))
        if pygame.mouse.get_pressed()[0] and buttonrect42.collidepoint(
                pygame.mouse.get_pos()):
            mc.harm()
            menu = "Q2"

    if menu == "A2":
        screen.blit(add3_image, (0, 0))
        txt43 = font1.render("맞습니다! TG는 이름에서부터 알 수 ", True, (255, 255, 255))
        txt431 = font1.render("있듯이 전체적으로 관련된 계열은 ", True, (255, 255, 255))
        txt432 = font1.render("공학 계열이나 활동은 동아리원들의", True, (255, 255, 255))
        txt433 = font1.render("진로에 맞춰 유연하게 하기 때문에", True, (255, 255, 255))
        txt434 = font1.render("다른 계열의 진로를 가진 학생들도 ", True, (255, 255, 255))
        txt435 = font1.render("동아리 활동 세부 능력 특기사항을 ", True, (255, 255, 255))
        txt436 = font1.render("특기사항을 진로에 맞게 작성할 수", True, (255, 255, 255))
        txt437 = font1.render("있습니다!", True, (255, 255, 255))
        screen.blit(txt43, (100, 50))
        screen.blit(txt431, (100, 150))
        screen.blit(txt432, (100, 250))
        screen.blit(txt433, (100, 350))
        screen.blit(txt434, (100, 450))
        screen.blit(txt435, (100, 550))
        screen.blit(txt436, (100, 650))
        screen.blit(txt437, (100, 750))

        if pressed_keys[K_5]:
            menu = "Q3"
        txt111111 = font1.render("5을 눌러 계속하기>>", True, (255, 255, 255))
        buttonrect111111 = pygame.Rect((300, 610), txt111111.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect111111)
        screen.blit(txt111111, (300, 610))

    if menu == "Q3":
        screen.blit(add3_image, (0, 0))
        txt45 = font1.render("숫자 5가 제일 싫어하는 집은?", True, (255, 255, 255))
        screen.blit(txt45, (150, 100))

        txt46 = font1.render("1. 우리집", True, (255, 255, 255))
        buttonrect46 = pygame.Rect((200, 250), txt46.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect46)
        screen.blit(txt46, (200, 250))
        if pygame.mouse.get_pressed()[0] and buttonrect46.collidepoint(
                pygame.mouse.get_pos()):
            menu = "Q3"

        txt47 = font1.render("2. 오페라하우스", True, (255, 255, 255))
        buttonrect47 = pygame.Rect((200, 350), txt47.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect47)
        screen.blit(txt47, (200, 350))
        if pygame.mouse.get_pressed()[0] and buttonrect47.collidepoint(
                pygame.mouse.get_pos()):
            menu = "A3"

        txt48 = font1.render("3. 오 님 좀 짱인듯 집", True, (255, 255, 255))
        buttonrect48 = pygame.Rect((200, 450), txt48.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect48)
        screen.blit(txt48, (200, 450))
        if pygame.mouse.get_pressed()[0] and buttonrect48.collidepoint(
                pygame.mouse.get_pos()):
            menu = "Q3"

    if menu == "A3":
        screen.blit(add3_image, (0, 0))
        txt49 = font1.render("맞습니다! 5는 오페라하우스(5를 패라", True, (255, 255, 255))
        txt491 = font1.render("집)을 싫어합니다 우리집을 싫어할", True, (255, 255, 255))
        txt492 = font1.render("오 님 좀 짱인듯 집은 어디일까요..?", True, (255, 255, 255))
        screen.blit(txt49, (100, 100))
        screen.blit(txt491, (100, 200))
        screen.blit(txt492, (100, 300))

        if pressed_keys[K_6]:
            menu = "Fin1"
        txt1111111 = font1.render("6을 눌러 계속하기>>", True, (255, 255, 255))
        buttonrect1111111 = pygame.Rect((300, 610), txt1111111.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect1111111)
        screen.blit(txt1111111, (300, 610))

    if menu == "Fin1":
        screen.blit(finish1_image, (0, 0))
        if pressed_keys[K_7]:
            menu = "Fin2"

        txt44444 = font1.render("7을 눌러 계속하기>>", True, (255, 255, 255))
        screen.blit(txt44444, (10, 620))
        buttonrect44444 = pygame.Rect((10, 620), txt44444.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect44444)
        screen.blit(txt44444, (10, 620))

    if menu == "Fin2":
        screen.blit(finish2_image, (0, 0))
        if pressed_keys[K_8]:
            menu = "Fin3"

        txt444444 = font1.render("8을 눌러 계속하기>>", True, (255, 255, 255))
        screen.blit(txt444444, (10, 620))
        buttonrect444444 = pygame.Rect((10, 620), txt444444.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect444444)
        screen.blit(txt444444, (10, 620))

    if menu == "Fin3":
        screen.blit(finish3_image, (0, 0))
        if pressed_keys[K_9]:
            menu = "Fin"

        txt4444444 = font1.render("9을 눌러 계속하기>>", True, (255, 255, 255))
        screen.blit(txt4444444, (10, 620))
        buttonrect4444444 = pygame.Rect((10, 620), txt4444444.get_size())
        pygame.draw.rect(screen, (72, 72, 72), buttonrect4444444)
        screen.blit(txt4444444, (10, 620))

    if menu == "Fin":
        screen.blit(fin_image, (0, 0))

    screen.blit(mc_lives[mc.lives - 1], (900, 600))
    if mc.lives == 0:
        menu = "gameover"
    if menu == "gameover":
        screen.blit(gameover_image, (0, 0))
        if pygame.mouse.get_pressed()[0] and pygame.Rect(
            (555, 444), (333, 88)).collidepoint(pygame.mouse.get_pos()):
            menu = "apilog"

    pygame.display.update()
    </code>
  </pre>
</div>
<style>
  #toggle-button1 {
    border-radius: 10px; /* 모서리를 둥글게 */
    padding: 10px 20px; /* 버튼 크기 조절 */
    background-color: #007bff; /* 버튼 배경색 */
    color: white; /* 텍스트 색 */
    border: none; /* 버튼 테두리 제거 */
    cursor: pointer; /* 마우스를 올리면 포인터 표시 */
  }
  #toggle-button1:hover {
    background-color: #0056b3; /* 마우스를 올렸을 때 색상 */
  }
  #code-block1 {
    background-color: #93B6F9;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-family: monospace;
  }
</style>
<script>
  document.getElementById('toggle-button1').addEventListener('click', function () {
    const codeBlock = document.getElementById('code-block1');
    if (codeBlock.style.display === 'none' || codeBlock.style.display === '') {
      codeBlock.style.display = 'block';
    } else {
      codeBlock.style.display = 'none';
    }
  });
</script>

국어 문법 상식 테스트 - 2022 동아리 발표회를 위한 밀양여자고등학교 IT 동아리 TG의 파이썬 팀의 프로젝트 결과물
<div>
  <button id="toggle-button2">국어 문법 상식 테스트 코드</button>
  <pre id="code-block2" style="display: none;">
    <code>
import pygame, sys, random, time
from pygame.locals import*
pygame.init()
screen = pygame.display.set_mode((1200,700))
font = pygame.font.SysFont("gulim",60)
score = 0
menu = "home"

home_image = pygame.image.load("images/home.png").convert()
Q1_image = pygame.image.load("images/Q1.png").convert()
Q2_image = pygame.image.load("images/Q2.png").convert()
Q3_image = pygame.image.load("images/Q3.png").convert()
Q4_image = pygame.image.load("images/Q4.png").convert()
A1_image = pygame.image.load("images/A1.png").convert()
A2_image = pygame.image.load("images/A2.png").convert()
A3_image = pygame.image.load("images/A3.png").convert()
A4_image = pygame.image.load("images/A4.png").convert()
prefect_image = pygame.image.load("images/perfect.jpg").convert()
ahah_image = pygame.image.load("images/ahah.jpg").convert()
half_image = pygame.image.load("images/half.jpg").convert()
quarter_image = pygame.image.load("images/quarter.jpg").convert()
foreigner_image = pygame.image.load("images/foreigner.jpg").convert()

while 1:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
            
    pressed_keys = pygame.key.get_pressed()

    if menu == "home":
        score = 0
        screen.blit(home_image,(0,0))
        txt = font.render("시작하기",True,(255,255,255))
        txt_x = 470
        txt_y = 430
        buttonrect = pygame.Rect((txt_x,txt_y), txt.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect)
        screen.blit(txt,(txt_x,txt_y))
        if pygame.mouse.get_pressed()[0] and buttonrect.collidepoint(pygame.mouse.get_pos()):
            menu = "Q1"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "Q1":
        screen.blit(Q1_image,(0,0))
        txt1 = font.render("[암날]",True,(255,255,255))
        buttonrect1 = pygame.Rect((250,500),txt1.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect1)
        screen.blit(txt1,(250,500))
        if pygame.mouse.get_pressed()[0] and buttonrect1.collidepoint(pygame.mouse.get_pos()):
            score += 25
            menu = "A1"
        txt2 = font.render("[압날]",True,(255,255,255))
        buttonrect2 = pygame.Rect((500,500),txt2.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect2)
        screen.blit(txt2,(500,500))
        if pygame.mouse.get_pressed()[0] and buttonrect2.collidepoint(pygame.mouse.get_pos()):
            menu = "A1"
        txt3 = font.render("[앞날]",True,(255,255,255))
        buttonrect3 = pygame.Rect((750,500),txt3.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect3)
        screen.blit(txt3,(750,500))
        if pygame.mouse.get_pressed()[0] and buttonrect3.collidepoint(pygame.mouse.get_pos()):
            menu = "A1"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "A1":
        screen.blit(A1_image,(0,0))
        txta = font.render("다음으로",True,(255,255,255))
        buttonrecta = pygame.Rect((txt_x,txt_y),txta.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrecta)
        screen.blit(txta,(txt_x,txt_y))
        if pygame.mouse.get_pressed()[0] and buttonrecta.collidepoint(pygame.mouse.get_pos()):
            menu = "Q2"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "Q2":
        screen.blit(Q2_image,(0,0))
        txt4 = font.render("1개",True,(255,255,255))
        buttonrect4 = pygame.Rect((150,500),txt4.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect4)
        screen.blit(txt4,(150,500))
        if pygame.mouse.get_pressed()[0] and buttonrect4.collidepoint(pygame.mouse.get_pos()):
            menu = "A2"
        txt5 = font.render("2개",True,(255,255,255))
        buttonrect5 = pygame.Rect((350,500),txt5.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect5)
        screen.blit(txt5,(350,500))
        if pygame.mouse.get_pressed()[0] and buttonrect5.collidepoint(pygame.mouse.get_pos()):
            menu = "A2"
        txt6 = font.render("3개",True,(255,255,255))
        buttonrect6 = pygame.Rect((550,500),txt6.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect6)
        screen.blit(txt6,(550,500))
        if pygame.mouse.get_pressed()[0] and buttonrect6.collidepoint(pygame.mouse.get_pos()):
            score += 25
            menu = "A2"
        txt7 = font.render("4개",True,(255,255,255))
        buttonrect7 = pygame.Rect((750,500),txt7.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect7)
        screen.blit(txt7,(750,500))
        if pygame.mouse.get_pressed()[0] and buttonrect7.collidepoint(pygame.mouse.get_pos()):
            menu = "A2"
        txt8 = font.render("5개",True,(255,255,255))
        buttonrect8 = pygame.Rect((950,500),txt8.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect8)
        screen.blit(txt8,(950,500))
        if pygame.mouse.get_pressed()[0] and buttonrect8.collidepoint(pygame.mouse.get_pos()):
            menu = "A2"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "A2":
        screen.blit(A2_image,(0,0))
        txtb = font.render("다음으로",True,(255,255,255))
        buttonrectb = pygame.Rect((txt_x,txt_y),txtb.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrectb)
        screen.blit(txtb,(txt_x,txt_y))
        if pygame.mouse.get_pressed()[0] and buttonrectb.collidepoint(pygame.mouse.get_pos()):
            menu = "Q3"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "Q3":
        screen.blit(Q3_image,(0,0))
        txt9 = font.render("백분률",True,(255,255,255))
        buttonrect9 = pygame.Rect((350,500),txt9.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect9)
        screen.blit(txt9,(350,500))
        if pygame.mouse.get_pressed()[0] and buttonrect9.collidepoint(pygame.mouse.get_pos()):
            menu = "A3"
        txt10 = font.render("백분율",True,(255,255,255))
        buttonrect10 = pygame.Rect((650,500),txt10.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect10)
        screen.blit(txt10,(650,500))
        if pygame.mouse.get_pressed()[0] and buttonrect10.collidepoint(pygame.mouse.get_pos()):
            score += 25
            menu = "A3"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
      
    if menu == "A3":
        screen.blit(A3_image,(0,0))
        txtc = font.render("다음으로",True,(255,255,255))
        buttonrectc = pygame.Rect((txt_x,txt_y),txtc.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrectc)
        screen.blit(txtc,(txt_x,txt_y))
        if pygame.mouse.get_pressed()[0] and buttonrectc.collidepoint(pygame.mouse.get_pos()):
            menu = "Q4"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
  
    if menu == "Q4":
        screen.blit(Q4_image,(0,0))
        txt_1 = font.render("많이 해주세요",True,(255,255,255))
        buttonrect_1 = pygame.Rect((250,400),txt_1.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_1)
        screen.blit(txt_1,(250,400))
        if pygame.mouse.get_pressed()[0] and buttonrect_1.collidepoint(pygame.mouse.get_pos()):
            menu = "A4"
        txt_2 = font.render("삼가주세요",True,(255,255,255))
        buttonrect_2 = pygame.Rect((750,400),txt_2.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_2)
        screen.blit(txt_2,(750,400))
        if pygame.mouse.get_pressed()[0] and buttonrect_2.collidepoint(pygame.mouse.get_pos()):
            menu = "A4"
        txt_3 = font.render("사랑해요",True,(255,255,255))
        buttonrect_3 = pygame.Rect((50,500),txt_3.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_3)
        screen.blit(txt_3,(50,500))
        if pygame.mouse.get_pressed()[0] and buttonrect_3.collidepoint(pygame.mouse.get_pos()):
            score += 25
            menu = "A4"
        txt_4 = font.render("많이해주세요",True,(255,255,255))
        buttonrect_4 = pygame.Rect((350,500),txt_4.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_4)
        screen.blit(txt_4,(350,500))
        if pygame.mouse.get_pressed()[0] and buttonrect_4.collidepoint(pygame.mouse.get_pos()):
            menu = "A4"
        txt_5 = font.render("삼가 주세요",True,(255,255,255))
        buttonrect_5 = pygame.Rect((800,500),txt_5.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_5)
        screen.blit(txt_5,(800,500))
        if pygame.mouse.get_pressed()[0] and buttonrect_5.collidepoint(pygame.mouse.get_pos()):
            score += 25
            menu = "A4"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))
      
    if menu == "A4":
        screen.blit(A4_image,(0,0))
        txtd = font.render("다음으로",True,(255,255,255))
        buttonrectd = pygame.Rect((txt_x,txt_y),txtd.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrectd)
        screen.blit(txtd,(txt_x,txt_y))
        if pygame.mouse.get_pressed()[0] and buttonrectd.collidepoint(pygame.mouse.get_pos()):
            menu = "finish"
  
    if menu == "finish":
        if score == 100:
            screen.blit(prefect_image,(0.0))
        elif score == 75:
            screen.blit(ahah_image,(0,0))
        elif score == 50:
            screen.blit(half_image,(0,0))
        elif score == 25:
            screen.blit(quarter_image,(0,0))
        else:
            screen.blit(foreigner_image,(0,0))
      
        txt_f = font.render("처음으로",True,(255,255,255))
        buttonrect_f = pygame.Rect((850,350), txt_f.get_size())
        pygame.draw.rect(screen,(72,72,72),buttonrect_f)
        screen.blit(txt_f,(850,350))
        if pygame.mouse.get_pressed()[0] and buttonrect_f.collidepoint(pygame.mouse.get_pos()):
            menu = "home"
        txt_j = font.render("점수 :",True,(0,0,0))
        txt_o = font.render(str(score),True,(0,0,0))
        screen.blit(txt_j,(0,0))
        screen.blit(txt_o,(200,0))

    pygame.display.update()

#시작하기-Q1-A1-Q2-A2-Q3-A3-Q4-A4-결과-처음으로
    </code>
  </pre>
</div>
<style>
  #toggle-button2 {
    border-radius: 10px; /* 모서리를 둥글게 */
    padding: 10px 20px; /* 버튼 크기 조절 */
    background-color: #007bff; /* 버튼 배경색 */
    color: white; /* 텍스트 색 */
    border: none; /* 버튼 테두리 제거 */
    cursor: pointer; /* 마우스를 올리면 포인터 표시 */
  }
  #toggle-button2:hover {
    background-color: #0056b3; /* 마우스를 올렸을 때 색상 */
  }
  #code-block2 {
    background-color: #93B6F9;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-family: monospace;
  }
</style>
<script>
  document.getElementById('toggle-button2').addEventListener('click', function () {
    const codeBlock = document.getElementById('code-block2');
    if (codeBlock.style.display === 'none' || codeBlock.style.display === '') {
      codeBlock.style.display = 'block';
    } else {
      codeBlock.style.display = 'none';
    }
  });
</script>

Spaceman - 2022년 개인 프로젝트의 결과물(Python으로 제작)
<div>
  <button id="toggle-button3">spaceman 코드</button>
  <pre id="code-block3" style="display: none;">
    <code>
import pygame, sys, random, time
from pygame.locals import *

pygame.init()
clock = pygame.time.Clock()
pygame.display.set_caption("Space Man")
screen = pygame.display.set_mode((1200, 700))
last_alien_spawn_time = 0
score = 0
font = pygame.font.SysFont("malgungothic", 40)
font_s = pygame.font.SysFont("gulim.ttc", 95)

space_image = pygame.image.load("images/space.jpg").convert()
alien_image = pygame.image.load("images/alien.png").convert_alpha()
spaceman_image = pygame.image.load("images/spaceman.png").convert_alpha()
missile_image = pygame.image.load("images/missile.png").convert_alpha()
game_over_image = pygame.image.load("images/gameover.png").convert()


class Alien:

    def __init__(self):
        self.y = random.randint(0, 630)
        self.x = -100
        self.dx = random.randint(2, 4)
        self.dy = random.choice((-1, 1)) * self.dx

    def move(self):
        self.dx += 0.00000000000001
        self.x += self.dx
        if self.x < 100:
            self.y += self.dy
        if self.x > 100 and self.x < 250:
            self.y += self.dy * (-1)
        if self.x > 250 and self.x < 400:
            self.y += self.dy
        if self.x > 400 and self.x < 550:
            self.y += self.dy * (-1)
        if self.x > 550 and self.x < 700:
            self.y += self.dy
        if self.x > 700 and self.x < 850:
            self.y += self.dy * (-1)
        if self.x > 850 and self.x < 900:
            self.y += self.dy
        if self.x > 900 and self.x < 1050:
            self.y += self.dy * (-1)
        if self.x > 1050 and self.x < 1200:
            self.y += self.dy

    def draw(self):
        screen.blit(alien_image, (self.x, self.y))

    def bounce(self):
        if self.y < 0 or self.y > 660:
            self.dy *= -1

    def touching(self, missile):
        return (self.x + 35 - missile.x + 4)**2 + (self.y + 22.5 - missile.y +
                                                   10)**2 < 1225

    def off_screen(self):
        return self.x > 1200

    def score(self):
        global score
        score += 10


class Spaceman:

    def __init__(self):
        self.y = 350

    def move(self):
        if pressed_keys[K_UP] and self.y > 0:
            self.y -= 5
        if pressed_keys[K_DOWN] and self.y < 600:
            self.y += 5

    def draw(self):
        screen.blit(spaceman_image, (1062, self.y))

    def fire(self):
        missiles.append(Missile(self.y - 50))

    def hit_by(self, alien):
        return (alien.x > 1030 and alien.y > self.y - 15
                and alien.y < self.y + 70)


class Missile:

    def __init__(self, y):
        self.x = 1062
        self.y = y

    def move(self):
        self.x -= 10

    def off_screen(self):
        return self.x < -8

    def draw(self):
        screen.blit(missile_image, (self.x + 25, self.y + 80))


aliens = []
spaceman = Spaceman()
missiles = []

while 1:
    clock.tick(60)
    pressed_keys = pygame.key.get_pressed()
    for event in pygame.event.get():
        if event.type == QUIT:
            sys.exit()
        if event.type == KEYDOWN and event.key == K_SPACE:
            spaceman.fire()

    if time.time() - last_alien_spawn_time > 0.5:
        aliens.append(Alien())
        last_alien_spawn_time = time.time()
    screen.blit(space_image, (0, 0))

    spaceman.move()
    spaceman.draw()

    i = 0
    while i < len(aliens):
        aliens[i].move()
        aliens[i].draw()
        aliens[i].bounce()
        if aliens[i].off_screen():
            del aliens[i]
            i -= 1
        i += 1

    i = 0
    while i < len(missiles):
        missiles[i].move()
        missiles[i].draw()
        if missiles[i].off_screen():
            del missiles[i]
            i -= 1
        i += 1

    i = 0
    while i < len(aliens):
        j = 0
        while j < len(missiles):
            if aliens[i].touching(missiles[j]):
                aliens[i].score()
                del aliens[i]
                del missiles[j]
                i -= 1
                break
            j += 1
        i += 1

    screen.blit(font.render("점수: " + str(score), True, (224, 254, 224)),
                (5, 5))

    for alien in aliens:
        if spaceman.hit_by(alien):
            screen.blit(game_over_image, (0, 0))
            screen.blit(font_s.render(str(score), True, (255, 255, 0)),
                        (650, 380))
            while 1:
                for event in pygame.event.get():
                    if event.type == QUIT:
                        sys.exit()
                pygame.display.update()

    pygame.display.update()
    </code>
  </pre>
</div>
<style>
  #toggle-button3 {
    border-radius: 10px; /* 모서리를 둥글게 */
    padding: 10px 20px; /* 버튼 크기 조절 */
    background-color: #007bff; /* 버튼 배경색 */
    color: white; /* 텍스트 색 */
    border: none; /* 버튼 테두리 제거 */
    cursor: pointer; /* 마우스를 올리면 포인터 표시 */
  }
  #toggle-button3:hover {
    background-color: #0056b3; /* 마우스를 올렸을 때 색상 */
  }
  #code-block3 {
    background-color: #93B6F9;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-family: monospace;
  }
</style>
<script>
  document.getElementById('toggle-button3').addEventListener('click', function () {
    const codeBlock = document.getElementById('code-block3');
    if (codeBlock.style.display === 'none' || codeBlock.style.display === '') {
      codeBlock.style.display = 'block';
    } else {
      codeBlock.style.display = 'none';
    }
  });
</script>

### C_GAME
C언어 테트리스 - 2022년 개인 프로젝트의 결과물(C언어로 제작)
<div>
  <button id="toggle-button4">C언어 테트리스 코드</button>
  <pre id="code-block4" style="display: none;">
    <code>
#include <stdio.h>
#include <windows.h>
#include <conio.h>
#include <time.h>

clock_t startDropT, endT, startGroundT;
int x = 8, y = 0;
RECT blockSize;
int blockForm, blockRotation = 0;
int key;

int block[7][4][4][4] = {
    {// T 블럭
     {
      {0, 0, 0, 0},
      {0, 1, 0, 0},
      {1, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 1, 0},
      {0, 1, 0, 0}},
     {{0, 0, 0, 0},
      {0, 0, 0, 0},
      {1, 1, 1, 0},
      {0, 1, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 0, 0}}},
    {// 번개 블럭
     {
      {0, 0, 0, 0},
      {0, 1, 1, 0},
      {1, 1, 0, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 1, 0},
      {1, 1, 0, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 0, 0}}},
    {// 번개 블럭 반대
     {
      {0, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 0, 0},
      {1, 1, 0, 0},
      {1, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 0, 0},
      {1, 1, 0, 0},
      {1, 0, 0, 0}}},
    {// 1자형 블럭
     {
      {0, 1, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 0, 0}},
     {{0, 0, 0, 0},
      {0, 0, 0, 0},
      {1, 1, 1, 1},
      {0, 0, 0, 0}},
     {{0, 1, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 0, 0}},
     {{0, 0, 0, 0},
      {0, 0, 0, 0},
      {1, 1, 1, 1},
      {0, 0, 0, 0}}},
    {// L자형 블럭
     {
      {0, 0, 0, 0},
      {1, 0, 0, 0},
      {1, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 1, 0, 0},
      {1, 0, 0, 0},
      {1, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 1, 1, 0},
      {0, 0, 1, 0},
      {0, 0, 0, 0}},
     {{0, 1, 0, 0},
      {0, 1, 0, 0},
      {1, 1, 0, 0},
      {0, 0, 0, 0}}},
    {// L자형 블럭 반대
     {
      {0, 0, 0, 0},
      {0, 0, 1, 0},
      {1, 1, 1, 0},
      {0, 0, 0, 0}},
     {{1, 0, 0, 0},
      {1, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 1, 1, 0},
      {1, 0, 0, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {1, 1, 0, 0},
      {0, 1, 0, 0},
      {0, 1, 0, 0}}},
    {// 네모 블럭
     {
      {0, 0, 0, 0},
      {0, 1, 1, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 1, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 1, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}},
     {{0, 0, 0, 0},
      {0, 1, 1, 0},
      {0, 1, 1, 0},
      {0, 0, 0, 0}}}};

// 게임 보드
// 세로 15+1(아래벽)칸, 가로 10+2(양쪽벽)칸
int space[15 + 1][10 + 2] =
    {
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1},
        {1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1}};

void Init();
void gotoXY(int x, int y);
void CreateRandomForm();
bool CheckCrash(int x, int y);
void DropBlock();
void BlockToGround();
void RemoveLine();
void DrawMap();
void DrawBlock();
void InputKey();

int main()
{
    Init();
    startDropT = clock();
    CreateRandomForm();
    while (true)
    {
        DrawMap();
        DrawBlock();
        DropBlock();
        BlockToGround();
        RemoveLine();
        InputKey();
    }
    return 0;
}

void Init()
{
    CONSOLE_CURSOR_INFO cursorInfo;
    cursorInfo.bVisible = 0;
    cursorInfo.dwSize = 1;
    SetConsoleCursorInfo(GetStdHandle(STD_OUTPUT_HANDLE), &cursorInfo);
    srand(time(NULL));
}

void gotoXY(int x, int y)
{
    COORD pos;
    pos.X = x;
    pos.Y = y;
    SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE), pos);
}

void CreateRandomForm()
{
    blockForm = rand() % 7;
}

bool CheckCrash(int x, int y)
{
    for (int i = 0; i < 4; i++)
    {
        for (int j = 0; j < 4; j++)
        {
            if (block[blockForm][blockRotation][i][j] == 1)
            {
                int t = space[i + y][j + x / 2];
                if (t == 1 || t == 2)
                {
                    return true;
                }
            }
        }
    }
    return false;
}

void DropBlock()
{
    endT = clock();
    if ((float)(endT - startDropT) >= 800)
    {
        if (CheckCrash(x, y + 1) == true)
            return;
        y++;
        startDropT = clock();
        startGroundT = clock();
        system("cls");
    }
}

void BlockToGround()
{
    if (CheckCrash(x, y + 1) == true)
    {
        if ((float)(endT - startGroundT) > 1500)
        {
            for (int i = 0; i < 4; i++)
            {
                for (int j = 0; j < 4; j++)
                {
                    if (block[blockForm][blockRotation][i][j] == 1)
                    {
                        space[i + y][j + x / 2] = 2;
                    }
                }
            }
            x = 8;
            y = 0;
            CreateRandomForm();
        }
    }
}

void RemoveLine()
{
    for (int i = 15; i >= 0; i--)
    {
        int cnt = 0;
        for (int j = 1; j < 11; j++)
        {
            if (space[i][j] == 2)
            {
                cnt++;
            }
        }
        if (cnt >= 10)
        {
            for (int j = 0; i - j >= 0; j++)
            {
                for (int x = 1; x < 11; x++)
                {
                    if (i - j - 1 >= 0)
                        space[i - j][x] = space[i - j - 1][x];
                    else
                        space[i - j][x] = 0;
                }
            }
        }
    }
}

void DrawMap()
{
    gotoXY(0, 0);
    for (int i = 0; i < 16; i++)
    {
        for (int j = 0; j < 12; j++)
        {
            if (space[i][j] == 1)
            {
                gotoXY(j * 2, i);
                printf("□");
            }
            else if (space[i][j] == 2)
            {
                gotoXY(j * 2, i);
                printf("■");
            }
        }
    }
}

void DrawBlock()
{
    for (int i = 0; i < 4; i++)
    {
        for (int j = 0; j < 4; j++)
        {
            if (block[blockForm][blockRotation][i][j] == 1)
            {
                gotoXY(x + j * 2, y + i);
                printf("■");
            }
        }
    }
}

void InputKey()
{
    if (_kbhit())
    {
        key = _getch();
        switch (key)
        {
        case 32: // space
            blockRotation++;
            if (blockRotation >= 4)
                blockRotation = 0;
            startGroundT = clock();
            break;
        case 75: // left
            if (CheckCrash(x - 2, y) == false)
            {
                x -= 2;
                startGroundT = clock();
            }
            break;
        case 77: // right
            if (CheckCrash(x + 2, y) == false)
            {
                x += 2;
                startGroundT = clock();
            }
            break;
        case 80: // down
            if (CheckCrash(x, y + 1) == false)
            {
                y++;
            }
            break;
        }
        system("cls");
    }
}
    </code>
  </pre>
</div>
<style>
  #toggle-button4 {
    border-radius: 10px; /* 모서리를 둥글게 */
    padding: 10px 20px; /* 버튼 크기 조절 */
    background-color: #007bff; /* 버튼 배경색 */
    color: white; /* 텍스트 색 */
    border: none; /* 버튼 테두리 제거 */
    cursor: pointer; /* 마우스를 올리면 포인터 표시 */
  }
  #toggle-button4:hover {
    background-color: #0056b3; /* 마우스를 올렸을 때 색상 */
  }
  #code-block4 {
    background-color: #93B6F9;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-family: monospace;
  }
</style>
<script>
  document.getElementById('toggle-button4').addEventListener('click', function () {
    const codeBlock = document.getElementById('code-block4');
    if (codeBlock.style.display === 'none' || codeBlock.style.display === '') {
      codeBlock.style.display = 'block';
    } else {
      codeBlock.style.display = 'none';
    }
  });
</script>
