---
description: Versão remota do método IMFContentProtectionManager::BeginEnableContent.
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: RemoteBeginEnableContent (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a39f11fbecaab436a6db82ccb2880a56a783ef1ec43f0db6b408bd870917cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238717"
---
# <a name="remotebeginenablecontent"></a>RemoteBeginEnableContent

Versão remota do método [**IMFContentProtectionManager::BeginEnableContent.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a>Comentários

Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método. O método não aparece na vtable para a interface . Se [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) for chamado entre limites de processo, a DLL de proxy/stub do Media Foundation converterá a chamada em uma chamada para o método remoto e a converterá de volta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid.lib</dt> </dl>                    |



## <a name="see-also"></a>Veja também

<dl> <dt>

[**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




