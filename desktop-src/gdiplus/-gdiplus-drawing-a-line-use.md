---
description: Este tópico demonstra como desenhar uma linha usando o GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Desenhar uma Linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036804"
---
# <a name="drawing-a-line"></a>Desenhar uma Linha

Este tópico demonstra como desenhar uma linha usando o GDI Plus.

Para desenhar uma linha no Windows GDI+ você precisa de um [**objeto Gráfico,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) um objeto [**Caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e um [**objeto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) O **objeto Graphics** fornece o [método DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e o objeto **Pen** contém atributos da linha, como cor e largura. O endereço do objeto **Pen** é passado como um argumento para o **método DrawLine.**

O programa a seguir, que desenha uma linha de (0, 0) para (200, 100), consiste em três funções: **WinMain,** **WndProc** e **OnPaint**. As **funções WinMain** **e WndProc** fornecem o código fundamental comum à maioria dos Windows aplicativos. Não há nenhum GDI+ código na **função WndProc.** A **função WinMain** tem uma pequena quantidade de código GDI+, ou seja, as chamadas necessárias para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). O GDI+ código que realmente cria um [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e desenha uma linha está na **função OnPaint.**

A **função OnPaint** recebe um handle para um contexto de dispositivo e passa esse manipular para [**um construtor gráfico.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) O argumento passado para o [**construtor Caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) é uma referência a um [**objeto**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Color. Os quatro números passados para o construtor de cores representam os componentes alfa, vermelho, verde e azul da cor. O componente alfa determina a transparência da cor; 0 é totalmente transparente e 255 é totalmente opaco. Os quatro números passados para o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) representam o ponto inicial (0, 0) e o ponto final (200, 100) da linha.


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



Observe a chamada para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) na **função WinMain.** O primeiro parâmetro da **função GdiplusStartup** é o endereço de um \_ PTR ULONG. **GdiplusStartup** preenche essa variável com um token que é passado posteriormente para a [**função GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) O segundo parâmetro da **função GdiplusStartup** é o endereço de uma [**estrutura GdiplusStartupInput.**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) O código anterior se baseia no construtor **GdiplusStartupInput** padrão para definir os membros da estrutura adequadamente.

 

 



