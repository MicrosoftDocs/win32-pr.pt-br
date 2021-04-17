---
description: O método IsUsingTimeFormat determina se um formato de hora especificado é o formato em uso no momento.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748194"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Método CSourceSeeking. IsUsingTimeFormat

O `IsUsingTimeFormat` método determina se um formato de hora especificado é o formato em uso no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Ponteiro para um GUID de formato de hora. Consulte [**GUIDs de formato de hora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                               | Descrição                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | O formato especificado não é o formato atual.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | O formato especificado é o formato atual.<br/>     |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/>                      |



 

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

 

 




