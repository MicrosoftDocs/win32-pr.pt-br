---
description: 'Versão remota do método IMFSourceResolver:: EndCreateObjectFromByteStream.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: RemoteEndCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce7e04368e099f00f0bd9d3f87141b5f8224f9c935f258ec9b4f7018cb7f364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974295"
---
# <a name="remoteendcreateobjectfrombytestream"></a>RemoteEndCreateObjectFromByteStream

Versão remota do método [**IMFSourceResolver:: EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) .

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a>Comentários

Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método. O método não aparece no vtable para a interface. Se [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




