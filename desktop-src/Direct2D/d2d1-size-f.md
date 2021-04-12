---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454863"
---
# <a name="d2d1_size_f"></a>D2D1 \_ tamanho \_ F

Armazena um par ordenado de floats, normalmente a largura e a altura de um retângulo.


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a>Comentários

Como pontos, os tamanhos são outro conceito de elementos gráficos importantes. Em Direct2D, os tamanhos são representados pelas estruturas de tamanho **\_ \_ F** ou [**d2d1 Size \_ \_ U**](d2d1-size-u.md) de d2d1. Ambos contêm um par ordenado de números, normalmente a largura e a altura de um retângulo. A **estrutura \_ \_ F de tamanho de d2d1** contém um par ordenado de valores **float** e a estrutura **\_ \_ U de tamanho de d2d1** contém um par ordenado de valores **UINT32** .

**D2d1 \_ TAMANHO \_ f** é um novo nome para um tipo já definido **D2D \_ tamanho \_ F**. Para obter uma lista dos campos fornecidos pelo **tamanho de d2d1 \_ \_ f**, consulte **D2D \_ Size \_ f**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2DBaseTypes. h (incluir D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D2D \_ tamanho \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[**D2D1 \_ tamanho \_ U**](d2d1-size-u.md)
</dt> <dt>

[**\_Ponto d2d1 \_ 2F**](d2d1-point-2f.md)
</dt> </dl>

 

