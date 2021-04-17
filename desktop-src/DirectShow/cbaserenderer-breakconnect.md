---
description: O método BreakConnect libera o pino de entrada de uma conexão.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787417"
---
# <a name="cbaserendererbreakconnect-method"></a>Método CBaseRenderer. BreakConnect

O `BreakConnect` método libera o pino de entrada de uma conexão.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                         | Descrição                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>             | O PIN não foi conectado.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Êxito.<br/>                    |
| <dl> <dt>**VFW \_ E \_ não \_ parado**</dt> </dl> | O filtro ainda está ativo.<br/> |



 

## <a name="remarks"></a>Comentários

O pino de entrada do filtro chama esse método de dentro de seu próprio `BreakConnect` método. (Para obter mais informações, consulte [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md).) O filtro executa alguma escrituração interna, como redefinir o sinalizador de fim de fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




