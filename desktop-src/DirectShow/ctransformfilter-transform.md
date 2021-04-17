---
description: O método Transform transforma um exemplo de entrada para produzir um exemplo de saída.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Método CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754220"
---
# <a name="ctransformfiltertransform-method"></a>Método CTransformFilter. Transform

O `Transform` método transforma um exemplo de entrada para produzir um exemplo de saída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Afixa* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de entrada.

</dd> <dt>

*pOut* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) da amostra de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A classe base retorna E \_ inesperada.

A classe derivada deve retornar um valor **HRESULT** , indicando êxito ou falha. Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Não entregar este exemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                    |



 

## <a name="remarks"></a>Comentários

Substitua esse método para produzir dados de saída. Leia os dados de entrada do exemplo especificado pelo parâmetro *pIn* e grave os novos dados no exemplo especificado pelo parâmetro *pout* .

Antes que o filtro Chame esse método, ele copia as propriedades do exemplo de entrada para o exemplo de saída. O `Transform` método deve definir todas as propriedades que diferem entre os dois exemplos, usando métodos **IMediaSample** ou a interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (se disponível).

Se o filtro não deve entregar este exemplo (por exemplo, para dar suporte ao controle de qualidade), o método deve retornar S \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




