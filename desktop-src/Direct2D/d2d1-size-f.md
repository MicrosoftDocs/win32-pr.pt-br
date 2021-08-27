---
title: D2D1_SIZE_F (D2DBaseTypes.h)
description: Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7068319c161d7d6b288da6d3a451d8cdfdda715b9890160d17cc7fe872322381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087756"
---
# <a name="d2d1_size_f"></a>D2D1 \_ TAMANHO \_ F

Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Comentários

Assim como os pontos, os tamanhos são outro conceito gráfico importante. No Direct2D, os tamanhos são representados pelas estruturas **D2D1 \_ SIZE \_ F** ou [**D2D1 \_ SIZE \_ U.**](d2d1-size-u.md) Ambos contêm um par ordenado de números, normalmente a largura e a altura de um retângulo. A **estrutura D2D1 \_ SIZE \_ F** contém um par ordenado de valores **FLOAT** e a estrutura **\_ D2D1 SIZE \_ U** contém um par ordenado de **valores UINT32.**

**D2D1 \_ SIZE \_ F** é um novo nome para um tipo já definido **D2D \_ SIZE \_ F.** Para ver uma lista dos campos fornecidos por **D2D1 \_ SIZE \_ F**, consulte **D2D \_ SIZE \_ F**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2DBaseTypes.h (inclua D2d1.h)</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D2D \_ SIZE \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ TAMANHO \_ U**](d2d1-size-u.md)
</dt> <dt>

[**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

