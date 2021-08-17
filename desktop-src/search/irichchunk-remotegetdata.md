---
description: Recupera o PROPVARIANT e a cadeia de caracteres de entrada que representa uma parte dos dados. Chamar esse método é o mesmo que chamar GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: Método IRichChunk::RemoteGetData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: caaa4ab9688ab8169bd0955c8abb1e976e7eb318e94875be1486e61b32e13207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862780"
---
# <a name="irichchunkremotegetdata-method"></a>Método IRichChunk::RemoteGetData

Recupera o [PROPVARIANT e](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) a cadeia de caracteres de entrada que representa uma parte dos dados. Chamar esse método é o mesmo que chamar [**GetData.**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFirstPos* \[ out\]
</dt> <dd>

Recebe a posição inicial baseada em zero do intervalo. Este parâmetro pode ser **NULL**.

</dd> <dt>

*pLength* \[ out\]
</dt> <dd>

Recebe o comprimento do intervalo. Este parâmetro pode ser **NULL**.

</dd> <dt>

*ppsz* \[ out\]
</dt> <dd>

Recebe o valor de cadeia de caracteres Unicode associado ou **NULL,** se não estiver disponível.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Recebe o valor [PROPVARIANT associado](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ou **VT \_ EMPTY,** se não estiver disponível. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
