---
description: Invoca o método que é chamado quando a operação assíncrona especificada relata o progresso.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke Method'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 141f79398e1f9f250b402df130daa728c8e2f0e5f78702d7866dbe9a202b5978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323115"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a>IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke Method

Invoca o método que é chamado quando a operação assíncrona especificada relata o progresso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*asyncInfo* \[ no\]
</dt> <dd>

Tipo: **[ **IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85))\***

A ação assíncrona que relata a conclusão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>           |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))
</dt> </dl>

 

 
