---
description: Construtor de CTransformInputPin. CTransformInputPin-método de construtor.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Construtor CTransformInputPin. CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76c19a883e7cfb416e557a23cf2a689e46dab36641ffc98cde5cbe5fe460f686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053566"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Construtor CTransformInputPin. CTransformInputPin

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pTransformFilter* 
</dt> <dd>

Ponteiro para o filtro que criou esse PIN, que deve ser um objeto [**CTransformFilter**](ctransformfilter.md) .

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

O parâmetro *pname* especifica o nome do PIN, que é retornado pelo método [**IPin:: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . No entanto, a cadeia de caracteres não é usada para o identificador de PIN. O identificador de PIN para esta classe é sempre "in". Para obter mais informações, consulte [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




