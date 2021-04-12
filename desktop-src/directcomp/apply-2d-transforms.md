---
title: Como aplicar transformações 2D
description: Este tópico demonstra como aplicar transformações 2D a um Visual usando o Microsoft DirectComposition.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- como aplicar transformações 2D DirectComposition
- Transformações 2D DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366508"
---
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="54d55-105">Como aplicar transformações 2D</span><span class="sxs-lookup"><span data-stu-id="54d55-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="54d55-106">Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="54d55-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="54d55-107">Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="54d55-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="54d55-108">Este tópico demonstra como aplicar transformações 2D a um Visual usando o Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="54d55-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="54d55-109">O exemplo neste tópico aplica-se a um grupo de transformações que:</span><span class="sxs-lookup"><span data-stu-id="54d55-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="54d55-110">Gire o Visual em 180 graus.</span><span class="sxs-lookup"><span data-stu-id="54d55-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="54d55-111">Escale verticalmente o Visual até três vezes seu tamanho original.</span><span class="sxs-lookup"><span data-stu-id="54d55-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="54d55-112">Traduza (mova) os pixels do Visual 150 à direita de sua posição original.</span><span class="sxs-lookup"><span data-stu-id="54d55-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="54d55-113">As capturas de tela a seguir mostram o Visual antes e depois de aplicar as transformações 2D.</span><span class="sxs-lookup"><span data-stu-id="54d55-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![resultado da aplicação de um grupo de transformações 2D a um Visual](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="54d55-115">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="54d55-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="54d55-116">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="54d55-116">Technologies</span></span>

-   [<span data-ttu-id="54d55-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="54d55-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="54d55-118">Elementos gráficos do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="54d55-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="54d55-119">DXGI (infraestrutura gráfica do DirectX)</span><span class="sxs-lookup"><span data-stu-id="54d55-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="54d55-120">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="54d55-120">Prerequisites</span></span>

-   <span data-ttu-id="54d55-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="54d55-121">C/C++</span></span>
-   <span data-ttu-id="54d55-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="54d55-122">Microsoft Win32</span></span>
-   <span data-ttu-id="54d55-123">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="54d55-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="54d55-124">Instruções</span><span class="sxs-lookup"><span data-stu-id="54d55-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="54d55-125">Etapa 1: inicializar objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="54d55-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="54d55-126">Crie o objeto de dispositivo e o objeto de destino de composição.</span><span class="sxs-lookup"><span data-stu-id="54d55-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="54d55-127">Crie um Visual, defina seu conteúdo e adicione-o à árvore visual.</span><span class="sxs-lookup"><span data-stu-id="54d55-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="54d55-128">Para obter mais informações, consulte [como inicializar o DirectComposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="54d55-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="54d55-129">Etapa 2: criar a matriz de grupo de transformação</span><span class="sxs-lookup"><span data-stu-id="54d55-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="54d55-130">Etapa 3: criar os objetos de transformação, definir suas propriedades e adicioná-los à matriz de grupos de transformação</span><span class="sxs-lookup"><span data-stu-id="54d55-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="54d55-131">Use os métodos [**IDCompositionDevice:: createrotatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: createscaletransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)e [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) para criar os objetos de transformação.</span><span class="sxs-lookup"><span data-stu-id="54d55-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="54d55-132">Use as funções de membro das interfaces [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)e [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) para definir as propriedades das transformações.</span><span class="sxs-lookup"><span data-stu-id="54d55-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="54d55-133">Copie os ponteiros da interface de transformação para a matriz do grupo de transformação.</span><span class="sxs-lookup"><span data-stu-id="54d55-133">Copy the transform interface pointers to the transform group array.</span></span>


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="54d55-134">Etapa 4: criar o objeto de grupo de transformação</span><span class="sxs-lookup"><span data-stu-id="54d55-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="54d55-135">Chame o método [**IDCompositionDevice:: CreateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Group para criar o objeto de grupo de transformação.</span><span class="sxs-lookup"><span data-stu-id="54d55-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="54d55-136">Etapa 5: aplicar o objeto de grupo de transformação ao Visual</span><span class="sxs-lookup"><span data-stu-id="54d55-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="54d55-137">Use o método [**IDCompositionVisual:: SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) para associar a propriedade Transform do Visual ao objeto do grupo de transformação.</span><span class="sxs-lookup"><span data-stu-id="54d55-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="54d55-138">Etapa 6: confirmar a composição</span><span class="sxs-lookup"><span data-stu-id="54d55-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="54d55-139">Chame o método [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar as atualizações para o Visual para DirectComposition para processamento.</span><span class="sxs-lookup"><span data-stu-id="54d55-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="54d55-140">O resultado da aplicação do grupo de transformações 2D aparece na janela de destino.</span><span class="sxs-lookup"><span data-stu-id="54d55-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="54d55-141">Etapa 7: liberar os objetos DirectComposition</span><span class="sxs-lookup"><span data-stu-id="54d55-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="54d55-142">Não se esqueça de liberar o grupo de objetos de transformação 2D quando não precisar mais deles.</span><span class="sxs-lookup"><span data-stu-id="54d55-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="54d55-143">O exemplo a seguir chama a macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida pelo aplicativo para liberar os objetos de transformação.</span><span class="sxs-lookup"><span data-stu-id="54d55-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="54d55-144">Lembre-se também de liberar o objeto de dispositivo, o objeto de destino de composição e os visuais antes de o aplicativo sair.</span><span class="sxs-lookup"><span data-stu-id="54d55-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="54d55-145">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="54d55-145">Complete example</span></span>


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="54d55-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54d55-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54d55-147">Transformações</span><span class="sxs-lookup"><span data-stu-id="54d55-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 