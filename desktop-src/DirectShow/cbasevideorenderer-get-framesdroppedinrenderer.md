---
description: O \_ método Get FramesDroppedInRenderer recupera o número de quadros descartados pelo renderizador.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Método de CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750667"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>CBaseVideoRenderer. obter \_ método FramesDroppedInRenderer

O `get_FramesDroppedInRenderer` método recupera o número de quadros descartados pelo renderizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

Ponteiro para o número de quadros descartados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualProp:: get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) . É assim que a página de propriedades recupera os dados do Agendador. Os quadros também podem ser retirados upstream sem o renderizador até mesmo vê-los.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




