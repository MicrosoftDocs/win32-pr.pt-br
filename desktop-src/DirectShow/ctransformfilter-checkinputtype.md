---
description: O método CheckInputType verifica se um tipo de mídia especificado é aceitável para entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter.CheckInputType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ef410ac8d96160b39ca9b7103e5125be8619169ba6b287a32b8769e57a0cbf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053616"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Método CTransformFilter.CheckInputType

O `CheckInputType` método verifica se um tipo de mídia especificado é aceitável para entrada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O tipo de mídia é aceitável.<br/>     |
| <dl> <dt>**TIPO VFW \_ E \_ NÃO \_ \_ ACEITO**</dt> </dl> | O tipo de mídia não é aceitável.<br/> |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. Retornar S \_ OK se o formato de entrada proposto for aceitável ou um código de erro, caso contrário.

Esse método não precisa verificar se o formato de entrada é compatível com o formato de saída (se há). O pino de entrada verifica isso chamando o [**método CheckTransform.**](ctransformfilter-checktransform.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




