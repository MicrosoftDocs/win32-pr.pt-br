---
title: D2D1_TAG (D2d1. h)
description: Um valor de 64 bits definido pelo aplicativo usado para \ 160; marque um conjunto de operações de renderização.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3dbea9f7c86f08a1c3c5df22b419bc5800db473aceed9f9a682a9d2e346a6a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108866"
---
# <a name="d2d1_tag"></a>Marca de D2D1 \_

Um valor de 64 bits definido pelo aplicativo usado para marcar um conjunto de operações de renderização.


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a>Comentários

Para definir uma marca antes de uma série de operações de renderização, use o método [**ID2D1RenderTarget:: settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) . Para recuperar a marca atual, use o método [**ID2D1RenderTarget:: gettags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos do Windows Server 2008 \[ desktop aplicativos \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**Settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

