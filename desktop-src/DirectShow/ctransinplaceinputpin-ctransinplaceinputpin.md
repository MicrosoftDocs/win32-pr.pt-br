---
description: Construtor CTransInPlaceInputPin.CTransInPlaceInputPin – Método de construtor.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Construtor CTransInPlaceInputPin.CTransInPlaceInputPin (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 266e67bc0d177aef592024236c87ab49c26cb81ef2264b4dde234232a3509006
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812766"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a>Construtor CTransInPlaceInputPin.CTransInPlaceInputPin

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CTransInPlaceInputPin(
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

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou esse pino, que deve ser um [**objeto CTransInPlaceFilter.**](ctransinplacefilter.md)

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método. Inicialize o valor como S \_ OK antes de criar o objeto . O valor será alterado somente se ocorrer um erro.

</dd> <dt>

*Pname* 
</dt> <dd>

Cadeia de caracteres largos que contém o nome do pino.

</dd> </dl>

## <a name="remarks"></a>Comentários

O *parâmetro pName* especifica o nome do pino, que é retornado pelo [**método IPin::QueryPinInfo.**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) No entanto, essa cadeia de caracteres não é usada para o identificador de pino. O identificador de pino para essa classe é sempre In. Para obter mais informações, [**consulte CTransformInputPin::QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




