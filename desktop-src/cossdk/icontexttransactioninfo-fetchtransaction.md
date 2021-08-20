---
description: Recupera a transação ou o proxy de transação associado ao contexto atual, se for o caso.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: Método IContextTransactionInfo::FetchTransaction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991056"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Método IContextTransactionInfo::FetchTransaction

Recupera a transação ou o proxy de transação associado ao contexto atual, se for o caso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnk* \[ out, retval\]
</dt> <dd>

O proxy de transação ou transação associado ao contexto atual; caso contrário, **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED e S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Servidor 2003 somente com aplicativos da área de trabalho SP1 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




