---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085326"
---
# <a name="d2d1_size_u"></a>D2D1 \_ tamanho \_ U

Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo.


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>Comentários

Como pontos, os tamanhos são outro conceito de elementos gráficos importantes. Em Direct2D, os tamanhos são representados pelas estruturas [**\_ \_ F**](d2d1-size-f.md) de tamanho **d2d1 \_ \_ U** ou d2d1 de tamanho. Ambos contêm um par ordenado de números. A **estrutura \_ \_ U de tamanho d2d1** contém um par ordenado de valores **UINT32** e a **estrutura \_ \_ F de tamanho d2d1** contém um par ordenado de valores **float** .

A **estrutura \_ \_ U de tamanho d2d1** fornece uma maneira conveniente de armazenar um par ordenado de números, como a largura e a altura de um retângulo.

**D2d1 \_ SIZE \_ u** é um novo nome para um tipo já definido **D2D \_ Size \_ U**. Você pode usar a função **d2d1:: sizeu** para criar uma **estrutura \_ \_ U de tamanho de d2d1** . Um uso comum para essa estrutura é especificar o tamanho do pixel de uma estrutura de [**\_ Propriedades de destino de \_ renderização \_ \_ d2d1 HWND**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) . Veja a seguir um exemplo de como usar essa estrutura.


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2DBaseTypes. h (incluir D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D2D \_ tamanho \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ tamanho \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

