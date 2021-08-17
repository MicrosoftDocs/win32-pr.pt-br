---
title: Como recortar com um objeto de clipe de retângulo
description: Este tópico demonstra como usar um objeto de clipe de retângulo para recortar uma árvore visual ou Visual.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10386f3e99dead7fff04a57463c2ee753bd1d712e9a59e6b928136c32f25ae75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119090"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Como recortar com um objeto de clipe de retângulo

> [!NOTE]
> para aplicativos no Windows 10, é recomendável usar as APIs Windows. UI. composição em vez de DirectComposition. Para obter mais informações, consulte [modernizar seu aplicativo de área de trabalho usando a camada Visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

Este tópico demonstra como usar um objeto de clipe de retângulo para recortar uma árvore visual ou Visual.

O exemplo neste tópico define um clipe retangular que é centralizado no local do mouse e aplica o clipe a um visual que é centralizado na área cliente da janela destino de composição. Esta captura de tela mostra o resultado da aplicação do objeto de clipe de retângulo ao Visual.

![resultado da aplicação de um objeto de clipe de retângulo a um Visual](images/clipwithrectangleclipobject.png)

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

### <a name="step-2-create-the-rectangle-clip-object"></a>Etapa 2: criar o objeto de clipe de retângulo

Use o método [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) para criar uma instância do objeto de clipe de retângulo.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Etapa 3: definir as propriedades do objeto de clipe de retângulo

Chame os métodos da interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) do objeto de clipe de retângulo para definir as propriedades do retângulo do clipe.

O exemplo a seguir define um retângulo de clipe que é centralizado em relação ao local atual do mouse. As `m_offsetX` `m_offsetY` variáveis de membro e contêm os valores das propriedades OffsetX e OffsetY do Visual.


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



Observe que a interface [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) inclui os seguintes métodos para definir um retângulo de clipe que tem cantos arredondados:

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Etapa 4: definir a propriedade de clipe do Visual

Use o método [**IDCompositionVisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) para associar a propriedade Clip do Visual ao objeto de clipe de retângulo.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Etapa 5: confirmar a composição

Chame o método [**IDCompositionDevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) para confirmar o lote de comandos para o Microsoft DirectComposition para processamento. O resultado da aplicação do clipe Rectangle é exibido na janela de destino.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Etapa 6: liberar os objetos DirectComposition

Certifique-se de liberar o objeto de clipe de retângulo quando você não precisar mais dele, bem como o objeto de dispositivo, o objeto de destino de composição e todos os objetos visuais. O exemplo a seguir chama a macro [**SafeRelease**](/windows/desktop/medfound/saferelease) definida pelo aplicativo para liberar os objetos DirectComposition.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recortando](clipping.md)
</dt> </dl>

 

 