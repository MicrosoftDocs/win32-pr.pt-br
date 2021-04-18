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
ms.openlocfilehash: 7f845ac7ae52537bfadfb6c913537b32e4d44171
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749819"
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

## <a name="return-value"></a>Retornar valor

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

Depois que o filtro soltar um quadro, ele continuará a descartar os quadros até atingir o próximo quadro-chave. Se esse método retornar **true**, ele também enviará um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Vtrans. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




