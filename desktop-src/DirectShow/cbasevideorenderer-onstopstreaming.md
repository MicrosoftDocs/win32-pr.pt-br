---
description: O método OnStopStreaming é chamado no final do streaming para corrigir os tempos para o relatório da página de propriedades.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Método CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782267"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Método CBaseVideoRenderer. OnStopStreaming

O `OnStopStreaming` método é chamado no final do streaming para corrigir os tempos para o relatório da página de propriedades.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro é chamada duas vezes, uma vez ao pausar e novamente quando o fluxo é realmente interrompido.

Essa função de membro substitui [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




