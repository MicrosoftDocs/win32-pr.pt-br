---
description: O método ScheduleSample substitui a classe base que faz o trabalho principal para manter uma contagem de amostras desenhada e descartada (que são usadas pela implementação de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Método CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658230"
---
# <a name="cbasevideorendererschedulesample-method"></a>Método CBaseVideoRenderer. ScheduleSample

O `ScheduleSample` método substitui a classe base que faz o trabalho principal manter uma contagem de amostras desenhada e descartada (que são usadas pela implementação de [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).

## <a name="syntax"></a>Sintaxe


```C++
BOOL ScheduleSample(
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

Retornará **true** se o exemplo for agendado; caso contrário, retornará **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




