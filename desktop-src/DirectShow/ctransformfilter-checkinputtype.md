---
description: O método CheckInputType verifica se um tipo de mídia especificado é aceitável para a entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter. CheckInputType (Transfrm. h)
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
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750037"
---
# <a name="ctransformfiltercheckinputtype-method"></a>Método CTransformFilter. CheckInputType

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

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | O tipo de mídia é aceitável.<br/>     |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | O tipo de mídia não é aceitável.<br/> |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. Retorne \_ os S ok se o formato de entrada proposto for aceitável ou um código de erro do contrário.

Esse método não precisa verificar se o formato de entrada é compatível com o formato de saída (se houver). O PIN de entrada verifica isso chamando o método [**CheckTransform**](ctransformfilter-checktransform.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




