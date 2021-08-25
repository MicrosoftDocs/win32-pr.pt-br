---
description: Recupera o nível de isolamento e o valor de tempo-máximo de uma transação que está hospedada no contexto de transação raiz.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: Método IContextTransactionInfo::GetTxIsolationLevelAndTimeout
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
ms.openlocfilehash: 41888a859b6b665390290ba66bed69418cbddd9b708355dc78cc2670ba4d240f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896076"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>Método IContextTransactionInfo::GetTxIsolationLevelAndTimeout

Recupera o nível de isolamento e o valor de tempo-máximo de uma transação que está hospedada no contexto de transação raiz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIsoLevel* \[ out\]
</dt> <dd>

O [valor ISOLATIONLEVEL](/previous-versions/windows/desktop/ms679234(v=vs.85)) para a transação.

</dd> <dt>

*dwTime* \[ out\]
</dt> <dd>

O tempoout da transação, em segundos.

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

 

