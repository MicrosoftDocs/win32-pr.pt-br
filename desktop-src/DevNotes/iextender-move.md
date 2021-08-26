---
description: Move um MDIForm, formulário ou controle.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: Método IExtender::Move
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
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002096"
---
# <a name="iextendermove-method"></a>Método IExtender::Move

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

*esquerda* \[ Em\]
</dt> <dd>

A borda esquerda do formulário ou controle.

</dd> <dt>

*top* \[ Em\]
</dt> <dd>

A borda superior do formulário ou controle.

</dd> <dt>

*largura* \[ Em\]
</dt> <dd>

A largura do formulário ou controle.

</dd> <dt>

*altura* \[ Em\]
</dt> <dd>

A altura do formulário ou controle.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




