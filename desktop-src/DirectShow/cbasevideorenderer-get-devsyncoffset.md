---
description: O \_ método Get DevSyncOffset recupera o desvio padrão do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado, para todos os quadros desde o início do streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Método de CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751697"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>CBaseVideoRenderer. obter \_ método DevSyncOffset

O `get_DevSyncOffset` método recupera o desvio padrão do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado, para todos os quadros desde o início do streaming.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piDev* 
</dt> <dd>

Ponteiro para o desvio padrão do tempo conforme descrito anteriormente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IQualProp:: get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




