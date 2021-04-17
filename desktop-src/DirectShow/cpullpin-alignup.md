---
description: O método AlignUp Arredonda um valor para cima até um limite de alinhamento especificado. Observação removida no Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Método CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789958"
---
# <a name="cpullpinalignup-method"></a>Método CPullPin. AlignUp

O método **AlignUp** Arredonda um valor para cima até um limite de alinhamento especificado.

> [!Note]  
> Removido do Windows 7.

 

## <a name="syntax"></a>Sintaxe


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*precisa* 
</dt> <dd>

Especifica o número a ser alinhado.

</dd> <dt>

*lAlign* 
</dt> <dd>

Especifica o limite de alinhamento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o resultado alinhado.

## <a name="remarks"></a>Comentários

> [!Caution]  
> Esse método pode causar estouro numérico se *ll* + (*LALIGN* -1) estouros.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




