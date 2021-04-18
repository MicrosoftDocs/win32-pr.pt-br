---
description: O método GetVideoPaletteEntries recupera um intervalo de entradas de paleta para o vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759452"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Método CBaseControlVideo. GetVideoPaletteEntries

O `GetVideoPaletteEntries` método recupera um intervalo de entradas de paleta para o vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartIndex* 
</dt> <dd>

Entrada da paleta inicial com base em zero.

</dd> <dt>

*Entradas* 
</dt> <dd>

Número de entradas necessárias.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Ponteiro para o número de cores obtidas.

</dd> <dt>

*pPalette* 
</dt> <dd>

Ponteiro para o buffer de saída para cores.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna NOERROR se for bem-sucedido, VFW \_ E \_ nenhuma \_ paleta \_ disponível se os exemplos de vídeo não tiverem paleta de cores, e \_ OUTOFMEMORY se não houver memória suficiente disponível, e \_ INVALIDARG se *startIndex* for inválido ou S false se não houver \_ nenhuma cor na paleta.

## <a name="remarks"></a>Comentários

Essa função de membro retorna a paleta atual do vídeo como uma matriz alocada pelo usuário. Para permanecer consistente, use os membros na estrutura **PaletteEntry** do Win32 para retornar as cores, em vez dos membros na estrutura **RGBQUAD** (embora o parâmetro seja um **longo**). A memória é alocada pelo chamador, portanto, basta copiar cada uma delas por vez. Determine se o número de entradas solicitadas e o deslocamento da posição inicial são válidos. Se o número de entradas for avaliado como zero, retorna um \_ código S falso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




