---
description: O método Transform transforma um exemplo em vigor.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter. Transform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758480"
---
# <a name="ctransinplacefiltertransform-method"></a>Método CTransInPlaceFilter. Transform

O `Transform` método transforma um exemplo em vigor.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Não entregar este exemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                    |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. Transforme os dados de exemplo em vigor. Se o filtro estiver usando dois alocadores, ele copiará os dados do exemplo de entrada para um novo exemplo e passará a cópia para esse método.

Se o filtro não deve entregar este exemplo (por exemplo, para dar suporte ao controle de qualidade), o método deve retornar S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




