---
description: Recupera o PROPVARIANT e a cadeia de caracteres de entrada que representa um bloco de dados. Chamar esse método é o mesmo que chamar GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Método IRichChunk:: RemoteGetData'
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
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090049"
---
# <a name="irichchunkremotegetdata-method"></a>Método IRichChunk:: RemoteGetData

Recupera o [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) e a cadeia de caracteres de entrada que representa um bloco de dados. Chamar esse método é o mesmo que chamar [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

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

*pFirstPos* \[ fora\]
</dt> <dd>

Recebe a posição inicial de base zero do intervalo. Este parâmetro pode ser **NULL**.

</dd> <dt>

*PLength* \[ fora\]
</dt> <dd>

Recebe o comprimento do intervalo. Este parâmetro pode ser **NULL**.

</dd> <dt>

*ppsz* \[ fora\]
</dt> <dd>

Recebe o valor de cadeia de caracteres Unicode associado ou **nulo** se não estiver disponível.

</dd> <dt>

*valores* \[ fora\]
</dt> <dd>

Recebe o valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associado ou **VT \_ vazio** se não estiver disponível. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
