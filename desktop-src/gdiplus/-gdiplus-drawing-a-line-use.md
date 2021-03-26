---
description: Este tópico demonstra como desenhar uma linha usando GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Desenhar uma Linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967774"
---
# <a name="drawing-a-line"></a>Desenhar uma Linha

Este tópico demonstra como desenhar uma linha usando GDI Plus.

Para desenhar uma linha no Windows GDI+, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e um objeto de [**cor**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . O objeto **Graphics** fornece o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , e o objeto **Pen** mantém os atributos da linha, como Color e Width. O endereço do objeto **Pen** é passado como um argumento para o método **DrawLine** .

O programa a seguir, que desenha uma linha de (0, 0) a (200, 100), consiste em três funções: **WinMain**, **WndProc** e **OnPaint**. As funções **WinMain** e **WndProc** fornecem o código fundamental comum para a maioria dos aplicativos do Windows. Não há nenhum código GDI+ na função **WndProc** . A função **WinMain** tem uma pequena quantidade de código GDI+, ou seja, as chamadas necessárias para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). O código GDI+ que realmente cria um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e desenha uma linha está na função **OnPaint** .

A função **OnPaint** recebe um identificador para um contexto de dispositivo e passa esse identificador para um construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . O argumento passado para o construtor de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) é uma referência a um objeto [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Os quatro números passados para o construtor de cores representam os componentes alfa, vermelho, verde e azul da cor. O componente alfa determina a transparência da cor; 0 é totalmente transparente e o 255 é totalmente opaco. Os quatro números passados para o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) representam o ponto inicial (0, 0) e o ponto final (200, 100) da linha.


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



Observe a chamada para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) na função **WinMain** . O primeiro parâmetro da função **GdiplusStartup** é o endereço de um ULONG \_ PTR. **GdiplusStartup** preenche essa variável com um token que é passado posteriormente para a função [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) . O segundo parâmetro da função **GdiplusStartup** é o endereço de uma estrutura [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) . O código anterior depende do construtor **GdiplusStartupInput** padrão para definir os membros da estrutura adequadamente.

 

 



