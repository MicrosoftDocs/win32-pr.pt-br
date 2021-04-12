---
description: Os critérios de filtro que regem a assinatura.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'Propriedade IEventSubscription2:: FilterCriteria'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089500"
---
# <a name="ieventsubscription2filtercriteria-property"></a>Propriedade IEventSubscription2:: FilterCriteria

Os critérios de filtro que regem a assinatura.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a>Valor da propriedade

Os critérios de filtro ou o CLSID para uma classe que implementa [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).

## <a name="error-codes"></a>Códigos do Erro

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ falha e S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




