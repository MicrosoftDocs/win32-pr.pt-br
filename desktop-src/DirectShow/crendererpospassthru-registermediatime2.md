---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual.
ms.assetid: 65755906-cf54-46d6-8149-5ad982be55f3
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
ms.openlocfilehash: ff741e58f74770c8a97c13252302d4ef86868af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751098"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a>Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)

O método [**RegisterMediaTime**](crendererpospassthru-registermediatime.md) armazena em cache os carimbos de data/hora do exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterMediaTime(
   LONGLONG StartTime,
   LONGLONG EndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartTime* 
</dt> <dd>

Hora de início da amostra, em unidades de 100 a nanossegundos.

</dd> <dt>

*EndTime* 
</dt> <dd>

Hora de término da amostra, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                          | Descrição         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Êxito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método armazena os valores de carimbo de data/hora fornecidos em *StartTime* e *EndTime*. O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.

O filtro deve chamar esse método para cada amostra que receber. O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




