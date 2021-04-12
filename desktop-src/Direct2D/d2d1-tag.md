---
title: D2D1_TAG (D2d1. h)
description: Um valor de 64 bits definido pelo aplicativo usado para \ 160; marque um conjunto de operações de renderização.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294799"
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
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[**Settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

