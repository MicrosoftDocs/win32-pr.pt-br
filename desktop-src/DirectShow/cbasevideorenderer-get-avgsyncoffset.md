---
description: O \_ método Get AvgSyncOffset recupera a média do tempo em milissegundos entre quando cada quadro esteve devido e quando foi realmente renderizado para todos os quadros desde o início do streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Método de CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759324"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>CBaseVideoRenderer. obter \_ método AvgSyncOffset

O `get_AvgSyncOffset` método recupera a média do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado para todos os quadros desde o início do streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piAvg* 
</dt> <dd>

Ponteiro para a média do tempo conforme descrito anteriormente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualProp:: get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




