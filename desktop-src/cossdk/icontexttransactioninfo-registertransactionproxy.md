---
description: Associa uma implementação de ITransactionProxy com o contexto atual.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Método IContextTransactionInfo:: RegisterTransactionProxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296127"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>Método IContextTransactionInfo:: RegisterTransactionProxy

Associa uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) com o contexto atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProxy* \[ no\]
</dt> <dd>

Uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) para associar ao contexto atual.

</dd> <dt>

*pGuid* \[ fora\]
</dt> <dd>

Um GUID que identifica o proxy de transação. O COM+ usa esse GUID ao chamar [**ITransactionProxy:: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) no proxy de transação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY E e e \_ inesperados, bem como os valores a seguir.



| Código de retorno                                                                                                     | Descrição                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                            | O método foi concluído com êxito.<br/>                                                                           |
| <dl> <dt>**CONTEXTO \_ E \_ ALREADYINTRANSACTION**</dt> </dl> | O contexto atual já tem uma implementação [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) associada.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>                       | O contexto atual está hospedando uma transação de BYOT (traga sua própria transação) ou uma transação não raiz.<br/>    |



 

## <a name="remarks"></a>Comentários

O método **RegisterTransactionProxy** só poderá ser chamado se o contexto atual for um contexto de transação raiz. Ele não poderá ser chamado se o contexto estiver hospedando uma transação de BYOT ou uma transação não raiz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




