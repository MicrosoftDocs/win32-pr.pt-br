---
description: A função CreateAudioMediaType Inicializa um tipo de mídia de uma estrutura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Função CreateAudioMediaType (mtype. h)
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
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812838"
---
# <a name="createaudiomediatype-function"></a>Função CreateAudioMediaType

A função **CreateAudioMediaType** Inicializa um tipo de mídia de uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

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

*PMT* 
</dt> <dd>

Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser inicializada.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Sinalizador que indica se o bloco de formato deve ser inicializado. Especifique **true** para inicializá-lo ou **false** caso contrário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna E \_ OUTOFMEMORY se não foi possível alocar a memória para os dados de formato; \_Caso contrário, ok.

## <a name="remarks"></a>Comentários

Se o parâmetro *bSetFormat* for **true**, o método alocará a memória para o bloco de formato. Se o parâmetro *PGTO* já contiver um bloco de formato alocado, ocorrerá um vazamento de memória. Para evitar um vazamento de memória, chame [**FreeMediaType**](freemediatype.md) antes de chamar essa função. Depois que o método retornar, chame **FreeMediaType** novamente para liberar o bloco de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de tipo de mídia**](media-type-functions.md)
</dt> </dl>

 

