---
description: 'Versão remota do método IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19d163e8f3e34a9d4b0eca70f70c15442f683450319243e80f3842548f78d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974275"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a>RemoteBeginRegisterPlatformWorkQueueWithMMCSS

Versão remota do método [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) .

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Comentários

Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método. O método não aparece no vtable para a interface. Se [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




