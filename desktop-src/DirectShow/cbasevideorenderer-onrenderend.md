---
description: O método OnRenderEnd executa a suavização para casos em que o tempo de renderização varia devido a interrupções.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Método CBaseVideoRenderer.OnRenderEnd (Renbase.h)
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
ms.openlocfilehash: 24d622ec62b27ae2e85eb9bef37516c82acbb17e03bef9a51b161edacd0b95c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658677"
---
# <a name="cbasevideorendereronrenderend-method"></a>Método CBaseVideoRenderer.OnRenderEnd

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função membro deve ser chamada logo após desenhar uma imagem.

Essa função membro substitui [**CBaseRenderer::OnRenderEnd.**](cbaserenderer-onrenderend.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




