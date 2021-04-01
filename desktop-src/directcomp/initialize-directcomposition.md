---
title: Como inicializar o DirectComposition
description: Este tópico demonstra como criar e inicializar o conjunto mínimo de objetos DirectComposition da Microsoft necessários para criar uma composição simples.
ms.assetid: F2BF9CE2-05EF-4345-A00E-F5C8A8660B24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8d248c3036bd0c901ee318ae0274809dafdf20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084776"
---
# <a name="how-to-initialize-directcomposition"></a><span data-ttu-id="fc916-103">Como inicializar o DirectComposition</span><span class="sxs-lookup"><span data-stu-id="fc916-103">How to initialize DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="fc916-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="fc916-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="fc916-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="fc916-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="fc916-106">Este tópico demonstra como criar e inicializar o conjunto mínimo de objetos DirectComposition da Microsoft necessários para criar uma composição simples.</span><span class="sxs-lookup"><span data-stu-id="fc916-106">This topic demonstrates how to create and initialize the minimum set of Microsoft DirectComposition objects needed to create a simple composition.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fc916-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="fc916-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fc916-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="fc916-108">Technologies</span></span>

-   [<span data-ttu-id="fc916-109">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="fc916-109">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="fc916-110">Elementos gráficos do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="fc916-110">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="fc916-111">DXGI (infraestrutura gráfica do DirectX)</span><span class="sxs-lookup"><span data-stu-id="fc916-111">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="fc916-112">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fc916-112">Prerequisites</span></span>

-   <span data-ttu-id="fc916-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="fc916-113">C/C++</span></span>
-   <span data-ttu-id="fc916-114">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="fc916-114">Microsoft Win32</span></span>
-   <span data-ttu-id="fc916-115">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="fc916-115">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="fc916-116">Instruções</span><span class="sxs-lookup"><span data-stu-id="fc916-116">Instructions</span></span>

### <a name="step-1-create-the-direct3d-device-object"></a><span data-ttu-id="fc916-117">Etapa 1: criar o objeto do dispositivo Direct3D</span><span class="sxs-lookup"><span data-stu-id="fc916-117">Step 1: Create the Direct3D device object</span></span>

<span data-ttu-id="fc916-118">Use a função [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) da API do Microsoft Direct3D para criar uma instância de um objeto de dispositivo que representa o adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc916-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) function from the Microsoft Direct3D API to create an instance of a device object that represents the display adapter.</span></span>


```C++
    ID3D11Device *m_pD3D11Device;


    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object. The D3D11_CREATE_DEVICE_BGRA_SUPPORT
    // flag enables rendering on surfaces using Direct2D.
    hr = D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT, 
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        nullptr);
```





### <a name="step-2-retrieve-a-pointer-to-the-dxgi-object"></a><span data-ttu-id="fc916-119">Etapa 2: recuperar um ponteiro para o objeto DXGI</span><span class="sxs-lookup"><span data-stu-id="fc916-119">Step 2: Retrieve a pointer to the DXGI object</span></span>

<span data-ttu-id="fc916-120">Use o método **QueryInterface** para recuperar o ponteiro [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) do objeto de dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="fc916-120">Use the **QueryInterface** method to retrieve the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) pointer from the Direct3D device object.</span></span> <span data-ttu-id="fc916-121">O DirectComposition usará o objeto de infraestrutura de gráficos do Microsoft DirectX (DXGI) para criar todos os objetos de superfície para o dispositivo DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="fc916-121">DirectComposition will use the Microsoft DirectX Graphics Infrastructure (DXGI) object to create all surface objects for the DirectComposition device.</span></span>


```C++
    IDXGIDevice *pDXGIDevice = nullptr;

    // Check the result of calling D3D11CreateDriver.
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }
```



### <a name="step-3-create-the-directcomposition-device-object"></a><span data-ttu-id="fc916-122">Etapa 3: criar o objeto de dispositivo DirectComposition</span><span class="sxs-lookup"><span data-stu-id="fc916-122">Step 3: Create the DirectComposition device object</span></span>

<span data-ttu-id="fc916-123">Use a função [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) para criar uma instância do objeto de dispositivo DirectComposition, especificando o ponteiro [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) recuperado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="fc916-123">Use the [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) function to create an instance of the DirectComposition device object, specifying the [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) pointer retrieved in the previous step.</span></span> <span data-ttu-id="fc916-124">A função recupera um ponteiro [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) usado para criar todos os outros objetos DirectComposition usados em uma composição.</span><span class="sxs-lookup"><span data-stu-id="fc916-124">The function retrieves an [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) pointer used to create all other DirectComposition objects used in a composition.</span></span>


```C++
    IDCompositionDevice *m_pDCompDevice;


    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDCompDevice));
    }
```





### <a name="step-4-create-the-composition-target-object"></a><span data-ttu-id="fc916-125">Etapa 4: criar o objeto de destino de composição</span><span class="sxs-lookup"><span data-stu-id="fc916-125">Step 4: Create the composition target object</span></span>

<span data-ttu-id="fc916-126">Use o método [**IDCompositionDevice:: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) para criar uma instância do objeto de destino de composição.</span><span class="sxs-lookup"><span data-stu-id="fc916-126">Use the [**IDCompositionDevice::CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) method to create an instance of the composition target object.</span></span> <span data-ttu-id="fc916-127">Chamar **CreateTargetForHwnd** associa o objeto de dispositivo à janela do aplicativo que exibirá a composição.</span><span class="sxs-lookup"><span data-stu-id="fc916-127">Calling **CreateTargetForHwnd** binds the device object to the application window that will display the composition.</span></span>


```C++
    IDCompositionTarget *m_pDCompTarget;


    if (SUCCEEDED(hr))
    {
        // Create the composition target object based on the 
        // specified application window.
        hr = m_pDCompDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pDCompTarget);   
    }
```





### <a name="step-5-create-a-visual-object"></a><span data-ttu-id="fc916-128">Etapa 5: criar um objeto visual</span><span class="sxs-lookup"><span data-stu-id="fc916-128">Step 5: Create a visual object</span></span>

<span data-ttu-id="fc916-129">Use o método [**IDCompositionDevice:: createvisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) para criar um objeto visual.</span><span class="sxs-lookup"><span data-stu-id="fc916-129">Use the [**IDCompositionDevice::CreateVisual**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual) method to create a visual object.</span></span> <span data-ttu-id="fc916-130">O método recupera um ponteiro [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) usado para definir as propriedades do Visual.</span><span class="sxs-lookup"><span data-stu-id="fc916-130">The method retrieves an [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) pointer used to set the properties of the visual.</span></span> <span data-ttu-id="fc916-131">Para obter mais informações, consulte [Propriedades de um objeto visual](basic-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="fc916-131">For more information, see [Properties of a visual object](basic-concepts.md).</span></span>


```C++
    IDCompositionVisual *pVisual = nullptr;

    // Create a visual object.          
    hr = m_pDCompDevice->CreateVisual(&pVisual);  
```



### <a name="step-6-create-a-composition-surface-and-render-a-bitmap-to-the-surface"></a><span data-ttu-id="fc916-132">Etapa 6: criar uma superfície de composição e renderizar um bitmap na superfície</span><span class="sxs-lookup"><span data-stu-id="fc916-132">Step 6: Create a composition surface and render a bitmap to the surface</span></span>

<span data-ttu-id="fc916-133">Crie um ponteiro [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) .</span><span class="sxs-lookup"><span data-stu-id="fc916-133">Create an [**IDCompositionSurface**](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface) pointer.</span></span>


```C++
    IDCompositionSurface *pSurface = nullptr;

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }
```



<span data-ttu-id="fc916-134">A função a seguir cria uma superfície do Microsoft DirectComposition e desenha o bitmap na superfície.</span><span class="sxs-lookup"><span data-stu-id="fc916-134">The following function creates a Microsoft DirectComposition surface and draws the bitmap on the surface.</span></span>


```C++
// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    if (ppSurface == nullptr)
        return E_INVALIDARG;

    // Get information about the bitmap.
    bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap. The DXGI_FORMAT_B8G8R8A8_UNORM flag is required for 
        // rendering on the surface using GDI via GetDC.
        hr = m_pDCompDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        hr = pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    if (SUCCEEDED(hr))
    {
        // Create a compatible DC and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    // Call an application-defined macro to free the surface pointer.
    SafeRelease(&pDXGISurface);

    return hr;
}
```



### <a name="step-7-bind-surface-to-visual-and-set-the-properties-of-the-visual-object"></a><span data-ttu-id="fc916-135">Etapa 7: associar a superfície ao Visual e definir as propriedades do objeto visual</span><span class="sxs-lookup"><span data-stu-id="fc916-135">Step 7: Bind surface to visual and set the properties of the visual object</span></span>

<span data-ttu-id="fc916-136">Chame os métodos da interface [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) do objeto visual para definir as propriedades do Visual.</span><span class="sxs-lookup"><span data-stu-id="fc916-136">Call the methods of the visual object's [**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual) interface to set the properties of the visual.</span></span>

<span data-ttu-id="fc916-137">Este exemplo a seguir define o conteúdo do bitmap para o Visual e a posição horizontal e vertical do Visual em relação ao canto superior esquerdo de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="fc916-137">This next example sets the bitmap content for the visual, and the horizontal and vertical position of the visual relative to upper-left corner of its container.</span></span> <span data-ttu-id="fc916-138">Como é o Visual raiz, o contêiner desse elemento visual é a janela de destino de composição.</span><span class="sxs-lookup"><span data-stu-id="fc916-138">Because it is the root visual, the container for this visual is the composition target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        hr = pVisual->SetOffsetX(xOffset);  
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(yOffset);  
        }
    }
```



### <a name="step-8-set-the-root-visual-of-the-visual-tree"></a><span data-ttu-id="fc916-139">Etapa 8: definir o Visual raiz da árvore visual</span><span class="sxs-lookup"><span data-stu-id="fc916-139">Step 8: Set the root visual of the visual tree</span></span>

<span data-ttu-id="fc916-140">Defina o Visual raiz da árvore visual chamando o método [**IDCompositionTarget:: SetRoot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) .</span><span class="sxs-lookup"><span data-stu-id="fc916-140">Set the root visual of the visual tree by calling the [**IDCompositionTarget::SetRoot**](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot) method.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pDCompTarget->SetRoot(pVisual);  
    }
```



### <a name="step-9-commit-the-composition"></a><span data-ttu-id="fc916-141">Etapa 9: confirmar a composição</span><span class="sxs-lookup"><span data-stu-id="fc916-141">Step 9: Commit the composition</span></span>

<span data-ttu-id="fc916-142">Chame o método [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar o lote de comandos para DirectComposition para processamento.</span><span class="sxs-lookup"><span data-stu-id="fc916-142">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to DirectComposition for processing.</span></span> <span data-ttu-id="fc916-143">A composição resultante é exibida na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="fc916-143">The resulting composition appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDCompDevice->Commit();  
    }
```



### <a name="step-10-free-the-directcomposition-objects"></a><span data-ttu-id="fc916-144">Etapa 10: liberar os objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="fc916-144">Step 10: Free the DirectComposition objects</span></span>

<span data-ttu-id="fc916-145">É uma boa prática de programação liberar qualquer objeto visual assim que você não precisar mais deles.</span><span class="sxs-lookup"><span data-stu-id="fc916-145">It is good programming practice to free any visual objects as soon as you no longer need them.</span></span> <span data-ttu-id="fc916-146">O exemplo a seguir chama a macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida pelo aplicativo para liberar o objeto visual.</span><span class="sxs-lookup"><span data-stu-id="fc916-146">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the visual object.</span></span>


```C++
    // Free the visual. 
    SafeRelease(&pVisual);
```



<span data-ttu-id="fc916-147">Além disso, lembre-se de liberar o objeto DXGI, o objeto de dispositivo e o objeto de destino de composição antes de o aplicativo sair.</span><span class="sxs-lookup"><span data-stu-id="fc916-147">Also, remember to free the DXGI object, the device object, and composition target object before your application exits.</span></span>


```C++
    SafeRelease(&pDXGIDevice);
```




```C++
    SafeRelease(&m_pDCompDevice);
    SafeRelease(&m_pDCompTarget);
    SafeRelease(&m_pD3D11Device);
```



## <a name="complete-example"></a><span data-ttu-id="fc916-148">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="fc916-148">Complete example</span></span>


```C++
//
// SimpleComposition.h
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

#pragma once
// Modify the following definitions if you need to target a platform prior to the ones specified below.
// Refer to MSDN for the latest info on corresponding values for different platforms.
#ifndef WINVER              // Allow use of features specific to Windows 7 or later.
#define WINVER 0x0700       // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT        // Allow use of features specific to Windows 7 or later.
#define _WIN32_WINNT 0x0700 // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN     // Exclude rarely-used items from Windows headers

// Windows Header Files:
#include <windows.h>

// C RunTime Header Files
#include <math.h>

// DirectComposition Header Files
#include <dcomp.h>

// Direct3D Header Files
#include <d3d11.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT InitializeDirectCompositionDevice();

    HRESULT CreateResources();
    void DiscardResources();

    HRESULT OnClientClick();

    HRESULT LoadResourceGDIBitmap(
        PCWSTR resourceName, 
        HBITMAP &hbmp
        );

    HRESULT MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface);

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;
    HBITMAP m_hBitmap;
    ID3D11Device *m_pD3D11Device;
    IDCompositionDevice *m_pDCompDevice;
    IDCompositionTarget *m_pDCompTarget;
 };


//
// SimpleComposition.cpp
//
// THIS CODE AND INFORMATION IS PROVIDED &quot;AS IS&quot; WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved

// Instructions: Right-click in the client area to cause DirectCompostion
// to create a simple composition consisting of a single GDI bitmap.

#include &quot;SimpleComposition.h&quot;

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE /* hInstance */,
    HINSTANCE /* hPrevInstance */,
    LPSTR /* lpCmdLine */,
    int /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                         *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL),
    m_hBitmap(NULL),
    m_pDCompDevice(nullptr),
    m_pDCompTarget(nullptr),
    m_pD3D11Device(nullptr)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()
{
    SafeRelease(&m_pDCompDevice);
    SafeRelease(&m_pDCompTarget);
    SafeRelease(&m_pD3D11Device);
}

/*******************************************************************
*                                                                  *
*  Create the application window.                                  *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = nullptr;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = L&quot;DirectCompDemoApp&quot;;

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        L&quot;DirectCompDemoApp&quot;,
        L&quot;DirectComposition Demo Application&quot;,
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);

        // Initialize DirectComposition resources, such as the
        // device object and composition target object.
        hr = InitializeDirectCompositionDevice();
    }

    if (SUCCEEDED(hr))
    {
        hr = CreateResources();
    }

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the DirectComposition device object and    *
*  and the composition target object. These objects endure for    *
*  the lifetime of the application.                               *
*                                                                 *
******************************************************************/

HRESULT DemoApp::InitializeDirectCompositionDevice()
{
    HRESULT hr = S_OK;

    D3D_FEATURE_LEVEL featureLevelSupported;

    // Create the D3D device object. The D3D11_CREATE_DEVICE_BGRA_SUPPORT
    // flag enables rendering on surfaces using Direct2D.
    hr = D3D11CreateDevice(
        nullptr,
        D3D_DRIVER_TYPE_HARDWARE,
        NULL,
        D3D11_CREATE_DEVICE_BGRA_SUPPORT, 
        NULL,
        0,
        D3D11_SDK_VERSION,
        &m_pD3D11Device,
        &featureLevelSupported,
        nullptr);

    IDXGIDevice *pDXGIDevice = nullptr;

    // Check the result of calling D3D11CreateDriver.
    if (SUCCEEDED(hr))
    {
        // Create the DXGI device used to create bitmap surfaces.
        hr = m_pD3D11Device->QueryInterface(&pDXGIDevice);
    }

    if (SUCCEEDED(hr))
    {
        // Create the DirectComposition device object.
        hr = DCompositionCreateDevice(pDXGIDevice, 
                __uuidof(IDCompositionDevice), 
                reinterpret_cast<void **>(&m_pDCompDevice));
    }
    if (SUCCEEDED(hr))
    {
        // Create the composition target object based on the 
        // specified application window.
        hr = m_pDCompDevice->CreateTargetForHwnd(m_hwnd, TRUE, &m_pDCompTarget);   
    }

    SafeRelease(&pDXGIDevice);

    return hr;
}

/******************************************************************
*                                                                 *
*  This method creates the GDI bitmap that the application gives  *
*  to DirectComposition to be composed.                           *
*                                                                 *
******************************************************************/

HRESULT DemoApp::CreateResources()
{
    HRESULT hr = S_OK;

    hr = LoadResourceGDIBitmap(L&quot;Logo&quot;, m_hBitmap);
   
    return hr;
}

/******************************************************************
*                                                                 *
*  Discard device-specific resources.                             *
*                                                                 *
******************************************************************/

void DemoApp::DiscardResources()
{
    DeleteObject(m_hBitmap);
}

/******************************************************************
*                                                                 *
*  The main window&#39;s message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}

/******************************************************************
*                                                                 *
*  Called whenever the user clicks in client area of the main     *
*  window. This method builds a simple visual tree and passes it  *   
*  to DirectComposition.
*                                                                 *
******************************************************************/

HRESULT DemoApp::OnClientClick()
{
    HRESULT hr = S_OK;
    float xOffset = 20; // horizonal position of visual
    float yOffset = 20; // vertical position of visual

    IDCompositionVisual *pVisual = nullptr;

    // Create a visual object.          
    hr = m_pDCompDevice->CreateVisual(&pVisual);  

    IDCompositionSurface *pSurface = nullptr;

    if (SUCCEEDED(hr))
    {
        // Create a composition surface and render a GDI bitmap 
        // to the surface.
        hr = MyCreateGDIRenderedDCompSurface(m_hBitmap, &pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the bitmap content of the visual. 
        hr = pVisual->SetContent(pSurface);
    }

    if (SUCCEEDED(hr))
    {
        // Set the horizontal and vertical position of the visual relative
        // to the upper-left corner of the composition target window.
        hr = pVisual->SetOffsetX(xOffset);  
        if (SUCCEEDED(hr))
        {
            hr = pVisual->SetOffsetY(yOffset);  
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the visual to be the root of the visual tree.          
        hr = m_pDCompTarget->SetRoot(pVisual);  
    }

    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDCompDevice->Commit();  
    }

    // Free the visual. 
    SafeRelease(&pVisual);

    return hr;
}

/******************************************************************
*                                                                 *
*  The window&#39;s message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {
            case WM_LBUTTONDOWN:
                {
                    pDemoApp->OnClientClick();
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                    pDemoApp->DiscardResources();
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
}

/******************************************************************
*                                                                 *
*  This method loads the specified GDI bitmap from the            *
*  application resources, creates a new bitmap that is in a       *
*  format that DirectComposition can use, and copies the contents *
*  of the original bitmap to the new bitmap.                      *
*                                                                 *
******************************************************************/

HRESULT DemoApp::LoadResourceGDIBitmap(PCWSTR resourceName, HBITMAP &hbmp)
{
    hbmp = static_cast<HBITMAP>(LoadImageW(HINST_THISCOMPONENT, resourceName, 
        IMAGE_BITMAP, 0, 0, LR_DEFAULTCOLOR));  
 
    return hbmp ? S_OK : E_FAIL;
}


// MyCreateGDIRenderedDCompSurface - Creates a DirectComposition surface and 
//   copies the bitmap to the surface. 
//
// Parameters:
//   hBitmap - a GDI bitmap.
//   ppSurface - the composition surface object.
//                                                                 
HRESULT DemoApp::MyCreateGDIRenderedDCompSurface(HBITMAP hBitmap, 
        IDCompositionSurface **ppSurface)
{
    HRESULT hr = S_OK;

    int bitmapWidth = 0;
    int bitmapHeight = 0;
    int bmpSize = 0;
    BITMAP bmp = { };
    HBITMAP hBitmapOld = NULL;

    HDC hSurfaceDC = NULL;  
    HDC hBitmapDC = NULL;

    IDXGISurface1 *pDXGISurface = nullptr;
    IDCompositionSurface *pDCSurface = nullptr;
    POINT pointOffset = { };

    if (ppSurface == nullptr)
        return E_INVALIDARG;

    // Get information about the bitmap.
    bmpSize = GetObject(hBitmap, sizeof(BITMAP), &bmp);

    hr = bmpSize ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        // Save the bitmap dimensions.
        bitmapWidth = bmp.bmWidth;
        bitmapHeight = bmp.bmHeight;

        // Create a DirectComposition-compatible surface that is the same size 
        // as the bitmap. The DXGI_FORMAT_B8G8R8A8_UNORM flag is required for 
        // rendering on the surface using GDI via GetDC.
        hr = m_pDCompDevice->CreateSurface(bitmapWidth, bitmapHeight, 
            DXGI_FORMAT_B8G8R8A8_UNORM, DXGI_ALPHA_MODE_IGNORE, &pDCSurface);
    }

    if (SUCCEEDED(hr)) 
    {
        // Begin rendering to the surface.
        hr = pDCSurface->BeginDraw(NULL, __uuidof(IDXGISurface1), 
            reinterpret_cast<void**>(&pDXGISurface), &pointOffset);
    }

    if (SUCCEEDED(hr)) 
    {
        // Get the device context (DC) for the surface.
        hr = pDXGISurface->GetDC(FALSE, &hSurfaceDC);
    }

    if (SUCCEEDED(hr))
    {
        // Create a compatible DC and select the surface 
        // into the DC.
        hBitmapDC = CreateCompatibleDC(hSurfaceDC);
        if (hBitmapDC != NULL)
        {
            hBitmapOld = (HBITMAP)SelectObject(hBitmapDC, hBitmap);
            BitBlt(hSurfaceDC, pointOffset.x, pointOffset.y, 
                bitmapWidth, bitmapHeight, hBitmapDC, 0, 0, SRCCOPY);
            
            if (hBitmapOld)
            {
                SelectObject(hBitmapDC, hBitmapOld);
            }
            DeleteDC(hBitmapDC);
        }

        pDXGISurface->ReleaseDC(NULL);
    }

    // End the rendering.
    pDCSurface->EndDraw();
    *ppSurface = pDCSurface;

    // Call an application-defined macro to free the surface pointer.
    SafeRelease(&pDXGISurface);

    return hr;
}

```





## <a name="related-topics"></a><span data-ttu-id="fc916-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc916-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc916-150">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="fc916-150">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)
</dt> <dt>

[<span data-ttu-id="fc916-151">**D3D11CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="fc916-151">**D3D11CreateDevice**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)
</dt> <dt>

[<span data-ttu-id="fc916-152">**IDCompositionDevice:: Commit**</span><span class="sxs-lookup"><span data-stu-id="fc916-152">**IDCompositionDevice::Commit**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[<span data-ttu-id="fc916-153">**IDCompositionDevice::CreateTargetForHwnd**</span><span class="sxs-lookup"><span data-stu-id="fc916-153">**IDCompositionDevice::CreateTargetForHwnd**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd)
</dt> <dt>

[<span data-ttu-id="fc916-154">**IDCompositionDevice:: createvisual**</span><span class="sxs-lookup"><span data-stu-id="fc916-154">**IDCompositionDevice::CreateVisual**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvisual)
</dt> <dt>

[<span data-ttu-id="fc916-155">**IDCompositionSurface**</span><span class="sxs-lookup"><span data-stu-id="fc916-155">**IDCompositionSurface**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionsurface)
</dt> <dt>

[<span data-ttu-id="fc916-156">**IDCompositionTarget:: SetRoot**</span><span class="sxs-lookup"><span data-stu-id="fc916-156">**IDCompositionTarget::SetRoot**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositiontarget-setroot)
</dt> <dt>

[<span data-ttu-id="fc916-157">**IDCompositionVisual:: setContent**</span><span class="sxs-lookup"><span data-stu-id="fc916-157">**IDCompositionVisual::SetContent**</span></span>](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)
</dt> <dt>

[<span data-ttu-id="fc916-158">**IDXGIDevice**</span><span class="sxs-lookup"><span data-stu-id="fc916-158">**IDXGIDevice**</span></span>](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)
</dt> <dt>

[<span data-ttu-id="fc916-159">**SafeRelease**</span><span class="sxs-lookup"><span data-stu-id="fc916-159">**SafeRelease**</span></span>](/windows/desktop/medfound/saferelease)
</dt> </dl>

 

 