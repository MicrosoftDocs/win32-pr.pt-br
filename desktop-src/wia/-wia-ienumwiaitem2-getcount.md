---
description: Retorna o número de elementos armazenados por este enumerador.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: Método IEnumWiaItem2::GetCount (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882416"
---
# <a name="ienumwiaitem2getcount-method"></a>Método IEnumWiaItem2::GetCount

Retorna o número de elementos armazenados por este enumerador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cElt* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Recebe um ponteiro para um **ULONG** que recebe o número de elementos na enumeração .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




