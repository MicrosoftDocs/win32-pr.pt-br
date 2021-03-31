---
description: Ignora o número especificado de itens durante uma enumeração de objetos IWiaItem2 disponíveis.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Método IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921073"
---
# <a name="ienumwiaitem2skip-method"></a>Método IEnumWiaItem2:: Skip

Ignora o número especificado de itens durante uma enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponíveis.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cElt* \[ no\]
</dt> <dd>

Tipo: **ULONG**

Especifica o número de itens a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




