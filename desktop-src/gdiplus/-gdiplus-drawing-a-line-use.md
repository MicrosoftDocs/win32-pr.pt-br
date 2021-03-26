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
# <a name="drawing-a-line"></a><span data-ttu-id="f0fbe-103">Desenhar uma Linha</span><span class="sxs-lookup"><span data-stu-id="f0fbe-103">Drawing a Line</span></span>

<span data-ttu-id="f0fbe-104">Este tópico demonstra como desenhar uma linha usando GDI Plus.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="f0fbe-105">Para desenhar uma linha no Windows GDI+, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e um objeto de [**cor**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="f0fbe-106">O objeto **Graphics** fornece o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) , e o objeto **Pen** mantém os atributos da linha, como Color e Width.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="f0fbe-107">O endereço do objeto **Pen** é passado como um argumento para o método **DrawLine** .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="f0fbe-108">O programa a seguir, que desenha uma linha de (0, 0) a (200, 100), consiste em três funções: **WinMain**, **WndProc** e **OnPaint**.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="f0fbe-109">As funções **WinMain** e **WndProc** fornecem o código fundamental comum para a maioria dos aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="f0fbe-110">Não há nenhum código GDI+ na função **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="f0fbe-111">A função **WinMain** tem uma pequena quantidade de código GDI+, ou seja, as chamadas necessárias para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span><span class="sxs-lookup"><span data-stu-id="f0fbe-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="f0fbe-112">O código GDI+ que realmente cria um objeto de [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e desenha uma linha está na função **OnPaint** .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="f0fbe-113">A função **OnPaint** recebe um identificador para um contexto de dispositivo e passa esse identificador para um construtor de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="f0fbe-114">O argumento passado para o construtor de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) é uma referência a um objeto [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="f0fbe-115">Os quatro números passados para o construtor de cores representam os componentes alfa, vermelho, verde e azul da cor.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="f0fbe-116">O componente alfa determina a transparência da cor; 0 é totalmente transparente e o 255 é totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="f0fbe-117">Os quatro números passados para o método [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) representam o ponto inicial (0, 0) e o ponto final (200, 100) da linha.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


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



<span data-ttu-id="f0fbe-118">Observe a chamada para [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) na função **WinMain** .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="f0fbe-119">O primeiro parâmetro da função **GdiplusStartup** é o endereço de um ULONG \_ PTR.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="f0fbe-120">**GdiplusStartup** preenche essa variável com um token que é passado posteriormente para a função [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="f0fbe-121">O segundo parâmetro da função **GdiplusStartup** é o endereço de uma estrutura [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) .</span><span class="sxs-lookup"><span data-stu-id="f0fbe-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="f0fbe-122">O código anterior depende do construtor **GdiplusStartupInput** padrão para definir os membros da estrutura adequadamente.</span><span class="sxs-lookup"><span data-stu-id="f0fbe-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



