---
description: 'O método Skip ignora um número especificado de Pins na sequência de enumeração. Esse método implementa o método IEnumPins:: Skip.'
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Método CEnumPins. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770290"
---
# <a name="cenumpinsskip-method"></a>Método CEnumPins. Skip

O `Skip` método ignora um número especificado de Pins na sequência de enumeração. Esse método implementa o método [**IEnumPins:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de Pins a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                    | Ignorado após o fim da sequência.<br/>                                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt> </dl> | O estado do filtro foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




