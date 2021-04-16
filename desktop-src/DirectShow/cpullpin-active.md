---
description: O método ativo cria um thread de trabalho que efetua pull dos dados do pino de saída. Esse método também confirma o alocador.
ms.assetid: 9efa20f3-7909-4d87-bfa8-314d055b80f8
title: Método CPullPin. Active (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 461f6554f828dc096029ee1e7a1832e12a7c262a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750467"
---
# <a name="cpullpinactive-method"></a>Método CPullPin. active

O método **ativo** cria um thread de trabalho que efetua pull dos dados do pino de saída. Esse método também confirma o alocador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                                   |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | A conexão do PIN não foi estabelecida corretamente.<br/>          |
| <dl> <dt>**E \_ falha**</dt> </dl>       | Não foi possível criar o thread ou o thread já existe.<br/> |



 

## <a name="remarks"></a>Comentários

Chame esse método quando o filtro proprietário se tornar ativo. (Se o PIN de entrada deriva de [**CBasePin**](cbasepin.md), substitua o método [**CBasePin:: active**](cbasepin-active.md) .)

Antes de chamar esse método, chame o método [**CPullPin:: Connect**](cpullpin-connect.md) para estabelecer a conexão com o pino de saída.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




