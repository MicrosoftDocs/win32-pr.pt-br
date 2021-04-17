---
description: Essa função recupera a versão da biblioteca offline do registro.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Função ORGetVersion (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748688"
---
# <a name="orgetversion-function"></a>Função ORGetVersion

Essa função recupera a versão da biblioteca offline do registro.

## <a name="syntax"></a>Sintaxe


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwMajorVersion* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável para receber a versão principal da biblioteca do registro offline. Para a versão inicial da biblioteca, o valor é 1.

</dd> <dt>

*pdwMinorVersion* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável para receber a versão secundária da biblioteca do registro offline. Para a versão inicial da biblioteca, o valor é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuível<br/> | Biblioteca de registro offline do Windows versão 1,0 ou posterior<br/>                      |
| parâmetro<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




