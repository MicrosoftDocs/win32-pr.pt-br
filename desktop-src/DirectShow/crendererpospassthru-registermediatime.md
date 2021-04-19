---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755588"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)

O método **RegisterMediaTime** armazena em cache os carimbos de data/hora do exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                        |
| <dl> <dt>**VFW \_ E \_ hora de mídia \_ \_ não \_ definida**</dt> </dl> | O exemplo não está com carimbo de data/hora.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método armazena os carimbos de data/hora do exemplo atual. O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.

O filtro deve chamar esse método para cada amostra que receber. O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




