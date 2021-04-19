---
description: O método StartStreaming inicia o streaming quando o filtro alterna para um estado de execução.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Método CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771859"
---
# <a name="cbaserendererstartstreaming-method"></a>Método CBaseRenderer. StartStreaming

O `StartStreaming` método inicia o streaming quando o filtro alterna para um estado de execução.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK ou outro valor **HRESULT** .

## <a name="remarks"></a>Comentários

Se o filtro tiver um exemplo, ele agendará o exemplo para renderização. Caso contrário, se houver uma notificação de fim de fluxo pendente, o filtro enviará um evento de [**\_ conclusão de EC**](ec-complete.md) para o Gerenciador de gráfico de filtro.

Esse método chama o método [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) . Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




