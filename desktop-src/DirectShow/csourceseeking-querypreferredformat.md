---
description: 'O método QueryPreferredFormat recupera o formato de hora preferencial do objeto. Esse método implementa o método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Método CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782851"
---
# <a name="csourceseekingquerypreferredformat-method"></a>Método CSourceSeeking. QueryPreferredFormat

O `QueryPreferredFormat` método recupera o formato de hora preferencial do objeto. Esse método implementa o método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Ponteiro para uma variável que recebe um GUID de formato de hora. Consulte [**GUIDs de formato de hora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Sucesso<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Valor de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




