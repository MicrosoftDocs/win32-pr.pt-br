---
description: Método CTransInPlaceOutputPin. CheckMediaType – o método CheckMediaType determina se o PIN aceita um tipo de mídia específico.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Método CTransInPlaceOutputPin. CheckMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2816d148af2a7514dc28a71036402f3781e47a0144848a2ea81bbb94d339f961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999026"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a>Método CTransInPlaceOutputPin. CheckMediaType

O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                 |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | Tipo de mídia não aceito.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CTransformOutputPin:: CheckMediaType**](ctransformoutputpin-checkmediatype.md) .

Se o filtro já estiver sendo transmitido e estiver usando dois alocadores, esse método rejeitará qualquer alteração de formato. Caso contrário, esse método chama o método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) do filtro para verificar o tipo de mídia. Se o pino de entrada estiver conectado, ele também chamará o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) no pino de saída upstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




