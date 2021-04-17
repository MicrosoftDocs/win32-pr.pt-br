---
description: 'O método FindPin recupera o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Método CSource. FindPin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fac8df1e53e4a129b42d1284a19392bc7b58aa2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749241"
---
# <a name="csourcefindpin-method"></a>Método CSource. FindPin

O `FindPin` método recupera o PIN com o identificador especificado. Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Id* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que identifica o PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN. Se o método falhar, \* *ppPin* será definido como **nulo**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>         | Argumento de ponteiro **nulo** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | Não foi possível encontrar um PIN com este identificador.<br/> |



 

## <a name="remarks"></a>Comentários

O primeiro PIN é sempre denominado "1"; o segundo PIN é denominado "2"; e assim por diante. Para obter mais informações, consulte [**CSourceStream:: QueryId**](csourcestream-queryid.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




