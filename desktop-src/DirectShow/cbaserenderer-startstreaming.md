---
description: O método StartStreaming inicia o streaming quando o filtro muda para um estado de execução.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Método CBaseRenderer.StartStreaming (Renbase.h)
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
ms.openlocfilehash: e8a9a70d403c4251c3250fc4d6f19c985a1546ea563a0d1bfe50ef7d7c6cfeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157483"
---
# <a name="cbaserendererstartstreaming-method"></a>Método CBaseRenderer.StartStreaming

O `StartStreaming` método inicia o streaming quando o filtro muda para um estado de execução.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK ou outro valor **HRESULT.**

## <a name="remarks"></a>Comentários

Se o filtro tiver um exemplo, ele agendará o exemplo para renderização. Caso contrário, se houver uma notificação de fim de fluxo pendente, o filtro enviará um evento [**EC \_ COMPLETE**](ec-complete.md) para o gerenciador de grafo de filtro.

Esse método chama o [**método CBaseRenderer::OnStartStreaming.**](cbaserenderer-onstartstreaming.md) Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




