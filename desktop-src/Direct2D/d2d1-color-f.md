---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Descreve os componentes vermelho, verde, azul e alfa de uma cor. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105812861"
---
# <a name="d2d1_color_f"></a>D2D1 \_ cor \_ F

Descreve os componentes vermelho, verde, azul e alfa de uma cor.


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>Comentários

**D2d1 \_ A cor \_ f** é um typedef para [**D2D \_ Color \_ f**](d2d-color-f.md), que, por sua vez, é um typedef para [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md). Para obter informações sobre os membros fornecidos pelo **d2d1 \_ Color \_ F**, consulte [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).

A classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fornece um conjunto de cores predefinidas e funções auxiliares para definir cores. Para obter mais informações, consulte a referência de [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar uma cor predefinida (preto) ao criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



O exemplo a seguir usa a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar uma cor usando valores vermelho, verde, azul e alfa.


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
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

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

