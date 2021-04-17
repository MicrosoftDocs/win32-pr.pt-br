---
description: Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Método IContextTransactionInfo:: GetTxIsolationLevelAndTimeout'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783686"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>Método IContextTransactionInfo:: GetTxIsolationLevelAndTimeout

Recupera o nível de isolamento e o valor de tempo limite de uma transação hospedada no contexto de transação raiz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIsoLevel* \[ fora\]
</dt> <dd>

O valor [ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) da transação.

</dd> <dt>

*dwTime* \[ fora\]
</dt> <dd>

O tempo limite da transação, em segundos.

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

 

