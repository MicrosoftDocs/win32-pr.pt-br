---
description: O método GetVideoPaletteEntries recupera um intervalo de entradas de paleta para o vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo.GetVideoPaletteEntries (Ctlutil.h)
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
ms.openlocfilehash: 5eb1c017353ed3e5095f5ee5d24870773c11211c14eaa44a673b4f12913c56c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057036"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a>Método CBaseControlVideo.GetVideoPaletteEntries

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

*Startindex* 
</dt> <dd>

Entrada da paleta inicial baseada em zero.

</dd> <dt>

*Entradas* 
</dt> <dd>

Número de entradas necessárias.

</dd> <dt>

*pRetrieved* 
</dt> <dd>

Ponteiro para o número de cores obtidas.

</dd> <dt>

*Ppalette* 
</dt> <dd>

Ponteiro para o buffer de saída para cores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna NOERROR se for bem-sucedido, VFW E NO PALETTE DISPONÍVEL se os exemplos de vídeo não têm nenhuma paleta de \_ \_ \_ \_ cores, E \_ OUTOFMEMORY se \_  não houver memória suficiente disponível, E INVALIDARG se StartIndex for inválido ou S FALSE se não houver cores \_ na paleta.

## <a name="remarks"></a>Comentários

Essa função membro retorna a paleta atual do vídeo como uma matriz alocada pelo usuário. Para permanecer consistente, use os membros na estrutura Win32 **PALETTEENTRY** para retornar as cores, em vez dos membros na estrutura **RGBQUAD** (embora o parâmetro seja **LONG).** A memória é alocada pelo chamador, portanto, basta copiar cada um por vez. Determine se o número de entradas solicitadas e o deslocamento de posição inicial são válidos. Se o número de entradas for avaliada como zero, retorne um código S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




