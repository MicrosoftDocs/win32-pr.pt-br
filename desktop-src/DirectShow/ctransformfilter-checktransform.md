---
description: O método CheckTransform verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Método CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747586"
---
# <a name="ctransformfilterchecktransform-method"></a>Método CTransformFilter. CheckTransform

O `CheckTransform` método verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mtIn* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de entrada.

</dd> <dt>

*mtOut* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Os tipos de mídia são compatíveis.<br/>     |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | Os tipos de mídia não são compatíveis.<br/> |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. Retorne \_ os S ok se o filtro puder aceitar os dois tipos de mídia especificados ou se um código de erro for diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




