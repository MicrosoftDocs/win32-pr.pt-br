---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)
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
ms.openlocfilehash: 69688bb011fc8a75b0ec52effaef3afd7972fb7a198a4cdedf20c07a40c4fa7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054376"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Método CRendererPosPassThru.RegisterMediaTime (Ctlutil.h)

O **método RegisterMediaTime** armazena em cache os carimbos de data/hora do exemplo atual.

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

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                        |
| <dl> <dt>**TEMPO DE MÍDIA DO VFW \_ E \_ NÃO \_ \_ \_ DEFINIDO**</dt> </dl> | O exemplo não tem carimbo de data/hora.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método armazena os carimbos de data/hora do exemplo atual. O [**método CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.

O filtro deve chamar esse método para cada amostra que recebe. O método é sobrecarregado para aceitar um ponteiro para o exemplo ou os próprios valores de carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




