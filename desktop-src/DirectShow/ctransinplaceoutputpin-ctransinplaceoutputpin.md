---
description: Construtor de CTransInPlaceOutputPin. CTransInPlaceOutputPin-método de construtor.
ms.assetid: fe7b2d62-0e6a-4253-b469-6cede5dc9bb1
title: Construtor CTransInPlaceOutputPin. CTransInPlaceOutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faf8b2cf0a4f1def8ea89ad04bd013d3867ff5a456e6c8922f72a078d860df92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654774"
---
# <a name="ctransinplaceoutputpinctransinplaceoutputpin-constructor"></a>Construtor CTransInPlaceOutputPin. CTransInPlaceOutputPin

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CTransInPlaceOutputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou esse PIN, que deve ser um objeto [**CTransInPlaceFilter**](ctransinplacefilter.md) .

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método. Inicialize o valor para S \_ OK antes de criar o objeto. O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres largos contendo o nome do PIN.

</dd> </dl>

## <a name="remarks"></a>Comentários

O parâmetro *pname* especifica o nome do PIN, que é retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . No entanto, a cadeia de caracteres não é usada para o identificador de PIN. O identificador de PIN para esta classe é sempre "out". Para obter mais informações, consulte [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




