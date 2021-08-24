---
description: A função CreateAudioMediaType inicializa um tipo de mídia de uma estrutura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Função CreateAudioMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908816"
---
# <a name="createaudiomediatype-function"></a>Função CreateAudioMediaType

A **função CreateAudioMediaType** inicializa um tipo de mídia de uma [**estrutura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwfx* 
</dt> <dd>

Ponteiro para a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fornecida.

</dd> <dt>

*Pgto* 
</dt> <dd>

Ponteiro para a [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser inicializada.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Sinalizador que indica se o bloco de formato deve ser inicializado. **Especifique TRUE** para inicializá-lo ou **FALSE caso** contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará E \_ OUTOFMEMORY se a memória não puder ser alocada para os dados de formato; S \_ OK caso contrário.

## <a name="remarks"></a>Comentários

Se o *parâmetro bSetFormat* for **TRUE,** o método alocará a memória para o bloco de formato. Se o *parâmetro pmt* já contiver um bloco de formato alocado, ocorrerá uma perda de memória. Para evitar uma perda de memória, [**chame FreeMediaType antes**](freemediatype.md) de chamar essa função. Depois que o método retornar, chame **FreeMediaType novamente** para liberar o bloco de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de tipo de mídia**](media-type-functions.md)
</dt> </dl>

 

