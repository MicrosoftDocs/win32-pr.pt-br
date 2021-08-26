---
description: O método ShouldSkipFrame determina se o filtro deve descartar um exemplo especificado.
ms.assetid: 49f86f7d-28b1-443e-a238-692da96d60fb
title: Método CVideoTransformFilter. ShouldSkipFrame (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.ShouldSkipFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26a0c35be9914641abfa053cd1ee00f46bb09222aecbebc55d45900331a2ee81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075936"
---
# <a name="cvideotransformfiltershouldskipframe-method"></a>Método CVideoTransformFilter. ShouldSkipFrame

O `ShouldSkipFrame` método determina se o filtro deve descartar um exemplo especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL ShouldSkipFrame(
   IMediaSample *pIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Afixa* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** se o filtro deve descartar este exemplo ou **false** se o filtro deve processar este exemplo.

## <a name="remarks"></a>Comentários

Esse método retornará **true** se as seguintes condições forem atendidas:

-   O exemplo tem carimbos de data/hora.
-   O tempo médio de decodificação é de, pelo menos, 25% da duração do quadro.
-   No momento, o renderizador é pelo menos um quadro atrasado, conforme relatado por meio de mensagens de qualidade.
-   Ignorar para o próximo quadro chave não fará com que o quadro chegue mais de um quadro no início.

Para fins deste cálculo, o filtro registra as seguintes informações conforme processa os dados:

-   O tempo médio de decodificação nos últimos 20 quadros (**m \_ itrAvgDecode**)
-   O número de quadros desde o último quadro chave (**m \_ nFramesSinceKeyFrame**)
-   Uma estimativa de quantos quadros existem entre quadros-chave (**m \_ nKeyFramePeriod**)

Depois que o filtro soltar um quadro, ele continuará a descartar os quadros até atingir o próximo quadro-chave. se esse método retornar **TRUE**, ele também enviará um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o filtro Graph Manager.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




