---
title: Detectando e acompanhando vários pontos de toque
description: Detectando e acompanhando vários pontos de toque
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Touch, vários pontos de toque
- detectando vários pontos de toque
- acompanhamento de vários pontos de toque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454230"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="a3ee8-106">Detectando e acompanhando vários pontos de toque</span><span class="sxs-lookup"><span data-stu-id="a3ee8-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="a3ee8-107">As etapas a seguir explicam como acompanhar vários pontos de toque usando o Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="a3ee8-108">Crie um aplicativo e habilite o Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="a3ee8-109">Adicione um manipulador para pontos de controle e [**\_ toque do WM**](wm-touchdown.md) .</span><span class="sxs-lookup"><span data-stu-id="a3ee8-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="a3ee8-110">Desenhe os pontos.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-110">Draw the points.</span></span>

<span data-ttu-id="a3ee8-111">Depois que o aplicativo estiver em execução, ele processará círculos sob cada toque.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="a3ee8-112">A captura de tela a seguir mostra como o aplicativo pode ser exibido durante a execução.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-112">The following screen shot shows how your application might look while running.</span></span>

![captura de tela mostrando um aplicativo que renderiza pontos de toque como círculos verdes e amarelos](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="a3ee8-114">Criar um aplicativo e habilitar o Windows Touch</span><span class="sxs-lookup"><span data-stu-id="a3ee8-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="a3ee8-115">Inicie com um aplicativo Microsoft Win32 usando o assistente de Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="a3ee8-116">Depois de concluir o assistente, adicione o suporte para mensagens de toque do Windows definindo a versão do Windows em targetver. h e incluindo Windows. h e windowsx. h em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="a3ee8-117">O código a seguir mostra como definir a versão do Windows em targetver. h.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-117">The following code shows how to set the Windows version in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



<span data-ttu-id="a3ee8-118">O código a seguir mostra como as diretivas include devem ser adicionadas.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="a3ee8-119">Além disso, você pode criar algumas variáveis globais que serão usadas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-119">Also, you can create some global variables that will be used later.</span></span>


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="a3ee8-120">Adicionar manipulador para \_ pontos de toque e faixa do WM</span><span class="sxs-lookup"><span data-stu-id="a3ee8-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="a3ee8-121">Primeiro, declare algumas variáveis que são usadas pelo manipulador [**de \_ toque do WM**](wm-touchdown.md) em [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3ee8-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="a3ee8-122">Agora, inicialize as variáveis usadas para armazenar pontos de toque e registre a janela para entrada por toque do método **InitInstance** .</span><span class="sxs-lookup"><span data-stu-id="a3ee8-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



<span data-ttu-id="a3ee8-123">Em seguida, manipule a mensagem de [**\_ toque do WM**](wm-touchdown.md) do método [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a3ee8-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="a3ee8-124">O código a seguir mostra uma implementação do manipulador para o **WM \_ Touch**.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> <span data-ttu-id="a3ee8-125">Para usar a função [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) , você deve ter suporte a DPI alto em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="a3ee8-126">Para obter mais informações sobre como dar suporte a DPI alto, consulte a seção [alta dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) do MSDN.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="a3ee8-127">Agora, quando um usuário tocar na tela, as posições que ele estiver tocando serão armazenadas na matriz Points.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="a3ee8-128">O membro **dwID** da estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) armazena um identificador que será dependente de hardware.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="a3ee8-129">Para resolver o problema do membro dwID que é dependente de hardware, o manipulador de casos de [**\_ toque do WM**](wm-touchdown.md) usa uma função, **GetContactIndex**, que mapeia o membro **dwID** da estrutura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) para um ponto que é desenhado na tela.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="a3ee8-130">O código a seguir mostra uma implementação dessa função.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-130">The following code shows an implementation of this function.</span></span>


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a><span data-ttu-id="a3ee8-131">Desenhar os pontos</span><span class="sxs-lookup"><span data-stu-id="a3ee8-131">Draw the Points</span></span>

<span data-ttu-id="a3ee8-132">Declare as variáveis a seguir para a rotina de desenho.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-132">Declare the following variables for the drawing routine.</span></span>


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



<span data-ttu-id="a3ee8-133">O contexto de exibição de memória *memDC* é usado para armazenar um contexto de gráfico temporário que é trocado pelo contexto de exibição renderizado, *HDC*, para eliminar a cintilação.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="a3ee8-134">Implemente a rotina de desenho, que usa os pontos que você armazenou e desenha um círculo nos pontos.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="a3ee8-135">O código a seguir mostra como você pode implementar o manipulador de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="a3ee8-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



<span data-ttu-id="a3ee8-136">Quando você executa o aplicativo, ele agora deve ser semelhante à ilustração no início desta seção.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="a3ee8-137">Para diversão, você pode desenhar algumas linhas extras em volta dos pontos de toque.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="a3ee8-138">A captura de tela a seguir mostra como o aplicativo pode parecer com algumas linhas extras desenhadas em volta dos círculos.</span><span class="sxs-lookup"><span data-stu-id="a3ee8-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![captura de tela mostrando um aplicativo que renderiza pontos de toque como círculos com linhas por meio dos centros e interseccionando as bordas dos pontos de toque](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="a3ee8-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3ee8-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ee8-141">Entrada por toque do Windows</span><span class="sxs-lookup"><span data-stu-id="a3ee8-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 