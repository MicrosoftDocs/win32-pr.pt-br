---
description: Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Método IContextTransactionInfo:: FetchTransaction'
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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089312"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Método IContextTransactionInfo:: FetchTransaction

Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*punk* \[ out, retval\]
</dt> <dd>

A transação ou o proxy de transação que está associado ao contexto atual; caso contrário, **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




