---
title: Como recortar com um objeto de clipe de retângulo
description: Este tópico demonstra como usar um objeto de clipe de retângulo para recortar uma árvore visual ou Visual.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008578"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="02307-103">Como recortar com um objeto de clipe de retângulo</span><span class="sxs-lookup"><span data-stu-id="02307-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="02307-104">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="02307-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="02307-105">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="02307-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="02307-106">Este tópico demonstra como usar um objeto de clipe de retângulo para recortar uma árvore visual ou Visual.</span><span class="sxs-lookup"><span data-stu-id="02307-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="02307-107">O exemplo neste tópico define um clipe retangular que é centralizado no local do mouse e aplica o clipe a um visual que é centralizado na área cliente da janela destino de composição.</span><span class="sxs-lookup"><span data-stu-id="02307-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="02307-108">Esta captura de tela mostra o resultado da aplicação do objeto de clipe de retângulo ao Visual.</span><span class="sxs-lookup"><span data-stu-id="02307-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![resultado da aplicação de um objeto de clipe de retângulo a um Visual](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="02307-110">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="02307-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="02307-111">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="02307-111">Technologies</span></span>

-   [<span data-ttu-id="02307-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="02307-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="02307-113">Elementos gráficos do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="02307-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="02307-114">DXGI (infraestrutura gráfica do DirectX)</span><span class="sxs-lookup"><span data-stu-id="02307-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="02307-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="02307-115">Prerequisites</span></span>

-   <span data-ttu-id="02307-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="02307-116">C/C++</span></span>
-   <span data-ttu-id="02307-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="02307-117">Microsoft Win32</span></span>
-   <span data-ttu-id="02307-118">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="02307-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="02307-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="02307-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="02307-120">Etapa 1: inicializar objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="02307-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="02307-121">Crie o objeto de dispositivo e o objeto de destino de composição.</span><span class="sxs-lookup"><span data-stu-id="02307-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="02307-122">Crie um Visual, defina seu conteúdo e adicione-o à árvore visual.</span><span class="sxs-lookup"><span data-stu-id="02307-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="02307-123">Para obter mais informações, consulte [como inicializar o DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="02307-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="02307-124">Etapa 2: criar o objeto de clipe de retângulo</span><span class="sxs-lookup"><span data-stu-id="02307-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="02307-125">Use o método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) para criar uma instância do objeto de clipe de retângulo.</span><span class="sxs-lookup"><span data-stu-id="02307-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="02307-126">Etapa 3: definir as propriedades do objeto de clipe de retângulo</span><span class="sxs-lookup"><span data-stu-id="02307-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="02307-127">Chame os métodos da interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) do objeto de clipe de retângulo para definir as propriedades do retângulo do clipe.</span><span class="sxs-lookup"><span data-stu-id="02307-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="02307-128">O exemplo a seguir define um retângulo de clipe que é centralizado em relação ao local atual do mouse.</span><span class="sxs-lookup"><span data-stu-id="02307-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="02307-129">As `m_offsetX` `m_offsetY` variáveis de membro e contêm os valores das propriedades OffsetX e OffsetY do Visual.</span><span class="sxs-lookup"><span data-stu-id="02307-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



<span data-ttu-id="02307-130">Observe que a interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) inclui os seguintes métodos para definir um retângulo de clipe que tem cantos arredondados:</span><span class="sxs-lookup"><span data-stu-id="02307-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="02307-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="02307-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="02307-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="02307-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="02307-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="02307-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="02307-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="02307-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="02307-135">Etapa 4: definir a propriedade de clipe do Visual</span><span class="sxs-lookup"><span data-stu-id="02307-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="02307-136">Use o método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para associar a propriedade Clip do Visual ao objeto de clipe de retângulo.</span><span class="sxs-lookup"><span data-stu-id="02307-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="02307-137">Etapa 5: confirmar a composição</span><span class="sxs-lookup"><span data-stu-id="02307-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="02307-138">Chame o método [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar o lote de comandos para o Microsoft DirectComposition para processamento.</span><span class="sxs-lookup"><span data-stu-id="02307-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="02307-139">O resultado da aplicação do clipe Rectangle é exibido na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="02307-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="02307-140">Etapa 6: liberar os objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="02307-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="02307-141">Certifique-se de liberar o objeto de clipe de retângulo quando você não precisar mais dele, bem como o objeto de dispositivo, o objeto de destino de composição e todos os objetos visuais.</span><span class="sxs-lookup"><span data-stu-id="02307-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="02307-142">O exemplo a seguir chama a macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida pelo aplicativo para liberar os objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="02307-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="02307-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02307-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02307-144">Recorte</span><span class="sxs-lookup"><span data-stu-id="02307-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 