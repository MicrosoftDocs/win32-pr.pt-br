---
description: 'Versão remota do método IMFContentProtectionManager:: EndEnableContent.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: RemoteEndEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827537"
---
# <a name="remoteendenablecontent"></a>RemoteEndEnableContent

Versão remota do método [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) .

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a>Comentários

Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método. O método não aparece no vtable para a interface. Se [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mfuuid. lib</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




