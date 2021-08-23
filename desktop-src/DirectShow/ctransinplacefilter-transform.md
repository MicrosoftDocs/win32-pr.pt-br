---
description: O método Transform transforma um exemplo no local.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter.Transform (Transip.h)
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
ms.openlocfilehash: 224052bc882792f57eedf9ea58842b953e5853012d3581ef14cad58467b614b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953395"
---
# <a name="ctransinplacefiltertransform-method"></a>Método CTransInPlaceFilter.Transform

O `Transform` método transforma um exemplo no local.

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

Ponteiro para a interface [**IMediaSample do**](/windows/desktop/api/Strmif/nn-strmif-imediasample) exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Não entregue este exemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                    |



 

## <a name="remarks"></a>Comentários

A classe derivada deve implementar esse método. Transforme os dados de exemplo no local. Se o filtro estiver usando dois alocadores, ele copiará os dados do exemplo de entrada para um novo exemplo e passará a cópia para esse método.

Se o filtro não deve fornecer este exemplo (por exemplo, para dar suporte ao controle de qualidade), o método deve retornar S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




