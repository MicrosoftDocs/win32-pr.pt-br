---
description: O método AgreeMediaType procura um tipo de mídia para fazer uma conexão de PIN.
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: Método CBasePin. AgreeMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753358"
---
# <a name="cbasepinagreemediatype-method"></a>Método CBasePin. AgreeMediaType

O `AgreeMediaType` método procura um tipo de mídia para fazer uma conexão de PIN.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica um tipo de mídia ou **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                            |
| <dl> <dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt> </dl> | Nenhum tipo de mídia aceitável foi encontrado.<br/> |



 

## <a name="remarks"></a>Comentários

Se o parâmetro *PGTO* for não **nulo** e especificar totalmente um tipo de mídia, esse método tentará uma conexão usando esse tipo de mídia. Se a tentativa falhar, o método retornará um erro.

Se o parâmetro *PGTO* for **nulo** ou especificar um tipo de mídia parcial, esse método tentará os tipos de mídia na seguinte ordem:

1.  Os tipos de mídia preferenciais do pino de recebimento.
2.  Os tipos de mídia preferenciais deste PIN.

Os tipos de mídia preferenciais são enumerados com o método [**CBasePin:: EnumMediaTypes**](cbasepin-enummediatypes.md) e o enumerador resultante é passado para o método [**CBasePin:: TryMediaTypes**](cbasepin-trymediatypes.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




