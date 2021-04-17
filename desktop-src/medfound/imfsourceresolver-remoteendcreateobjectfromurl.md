---
description: 'Versão remota do método IMFSourceResolver:: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797980"
---
# <a name="remoteendcreateobjectfromurl"></a>RemoteEndCreateObjectFromURL

Versão remota do método [**IMFSourceResolver:: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Comentários

Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método. O método não aparece no vtable para a interface. Se [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                                              |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




