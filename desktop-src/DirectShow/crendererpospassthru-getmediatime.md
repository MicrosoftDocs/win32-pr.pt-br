---
description: O método GetMediaTime recupera os carimbos de data/hora no exemplo atual.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755341"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Método CRendererPosPassThru. GetMediaTime

O `GetMediaTime` método recupera os carimbos de data/hora no exemplo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStartTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de início, em unidades do formato de hora atual.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de término, em unidades do formato de hora atual. Pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Não há suporte para a conversão para esse formato.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/>                  |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) . Os valores de carimbo de data/hora são convertidos no formato de hora atual chamando o método [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




