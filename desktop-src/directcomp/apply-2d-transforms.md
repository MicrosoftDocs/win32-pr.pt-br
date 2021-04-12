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
# <a name="how-to-apply-2d-transforms"></a>Como aplicar transformações 2D

> [!NOTE]
> Para aplicativos no Windows 10, é recomendável usar APIs do Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico demonstra como aplicar transformações 2D a um Visual usando o Microsoft DirectComposition. O exemplo neste tópico aplica-se a um grupo de transformações que:

1.  Gire o Visual em 180 graus.
2.  Escale verticalmente o Visual até três vezes seu tamanho original.
3.  Traduza (mova) os pixels do Visual 150 à direita de sua posição original.

As capturas de tela a seguir mostram o Visual antes e depois de aplicar as transformações 2D.

![resultado da aplicação de um grupo de transformações 2D a um Visual](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [DirectComposition](directcomposition-portal.md)
-   [Elementos gráficos do Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DXGI (infraestrutura gráfica do DirectX)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Microsoft Win32
-   COM (Component Object Model)

## <a name="instructions"></a>Instruções

### <a name="step-1-initialize-directcomposition-objects"></a>Etapa 1: inicializar objetos DirectComposition

1.  Crie o objeto de dispositivo e o objeto de destino de composição.
2.  Crie um Visual, defina seu conteúdo e adicione-o à árvore visual.

Para obter mais informações, consulte [como inicializar o DirectComposition](initialize-directcomposition.md).

### <a name="step-2-create-the-transform-group-array"></a>Etapa 2: criar a matriz de grupo de transformação


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a>Etapa 3: criar os objetos de transformação, definir suas propriedades e adicioná-los à matriz de grupos de transformação

1.  Use os métodos [**IDCompositionDevice:: createrotatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: createscaletransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)e [**:: CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) para criar os objetos de transformação.
2.  Use as funções de membro das interfaces [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)e [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) para definir as propriedades das transformações.
3.  Copie os ponteiros da interface de transformação para a matriz do grupo de transformação.


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



### <a name="step-4-create-the-transform-group-object"></a>Etapa 4: criar o objeto de grupo de transformação

Chame o método [**IDCompositionDevice:: CreateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) Group para criar o objeto de grupo de transformação.


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a>Etapa 5: aplicar o objeto de grupo de transformação ao Visual

Use o método [**IDCompositionVisual:: SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) para associar a propriedade Transform do Visual ao objeto do grupo de transformação.


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a>Etapa 6: confirmar a composição

Chame o método [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar as atualizações para o Visual para DirectComposition para processamento. O resultado da aplicação do grupo de transformações 2D aparece na janela de destino.


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a>Etapa 7: liberar os objetos DirectComposition

Não se esqueça de liberar o grupo de objetos de transformação 2D quando não precisar mais deles. O exemplo a seguir chama a macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida pelo aplicativo para liberar os objetos de transformação.


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



Lembre-se também de liberar o objeto de dispositivo, o objeto de destino de composição e os visuais antes de o aplicativo sair.

## <a name="complete-example"></a>Exemplo completo


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações](transforms.md)
</dt> </dl>

 

 