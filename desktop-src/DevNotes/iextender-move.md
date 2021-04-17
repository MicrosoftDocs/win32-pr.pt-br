---
description: Move um MDIForm, formulário ou controle.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'Método IExtender:: move'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 2c7ed806629f0e5e1bb0cdee5c76910728fd651d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752570"
---
# <a name="iextendermove-method"></a>Método IExtender:: move

Move um MDIForm, formulário ou controle.

## <a name="syntax"></a>Sintaxe


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*à esquerda* \[ no\]
</dt> <dd>

A borda esquerda do formulário ou controle.

</dd> <dt>

*superior* \[ no\]
</dt> <dd>

A borda superior do formulário ou controle.

</dd> <dt>

*largura* \[ no\]
</dt> <dd>

A largura do formulário ou controle.

</dd> <dt>

*altura* \[ no\]
</dt> <dd>

A altura do formulário ou controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




