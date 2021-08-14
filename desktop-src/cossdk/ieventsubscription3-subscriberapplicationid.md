---
description: O GUID do aplicativo do assinante.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: Propriedade IEventSubscription3::SubscriberApplicationID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 723a64b4e34c58b49f0ffa0851af836a536ff86ea23ee1b966a8ec243267950c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306364"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a>Propriedade IEventSubscription3::SubscriberApplicationID

O GUID do aplicativo do assinante.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que contém o GUID do aplicativo assinante.

## <a name="error-codes"></a>Códigos do Erro

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL e S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSubscription3**](ieventsubscription3.md)
</dt> </dl>

 

 




