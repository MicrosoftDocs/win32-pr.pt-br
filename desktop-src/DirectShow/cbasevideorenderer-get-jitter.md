---
description: O \_ método obter tremulação recupera o desvio padrão do tempo em milissegundos entre cada quadro e o próximo para todos os quadros desde o início do streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Método de CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787000"
---
# <a name="cbasevideorendererget_jitter-method"></a>Método de variação CBaseVideoRenderer. get \_

O `get_Jitter` método recupera o desvio padrão de tempo em milissegundos entre cada quadro e o próximo para todos os quadros desde o streaming iniciado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*piJitter* 
</dt> <dd>

Ponteiro para o desvio padrão do tempo entre quadros, em milissegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método de [**\_ variação IQualProp:: Get**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




