---
description: O método OnRenderEnd executa a suavização para casos em que o tempo de renderização varia devido a interrupções.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Método CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748634"
---
# <a name="cbasevideorendereronrenderend-method"></a>Método CBaseVideoRenderer. OnRenderEnd

O `OnRenderEnd` método executa a suavização para casos em que o tempo de renderização varia devido a interrupções.

## <a name="syntax"></a>Sintaxe


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para o exemplo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro deve ser chamada logo após o desenho de uma imagem.

Essa função de membro substitui [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




