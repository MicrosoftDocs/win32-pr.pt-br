---
description: Dada uma lista de tipos de mídia, o método TryMediaTypes tenta concluir uma conexão usando um desses tipos.
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: Método CBasePin. TryMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a4d4e33ca339c1ade344bb2ca9531bea381d14b4381773673b07e522437e90a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108616"
---
# <a name="cbasepintrymediatypes-method"></a>Método CBasePin. TryMediaTypes

Dada uma lista de tipos de mídia, o `TryMediaTypes` método tenta concluir uma conexão usando um desses tipos.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
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

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que limita os tipos de mídia possíveis, ou **NULL**.

</dd> <dt>

*pEnum* 
</dt> <dd>

Ponteiro para uma interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) , usado para enumerar a lista de tipos de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                                  | Descrição                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                               |
| <dl> <dt>**VFW \_ E \_ nenhum \_ \_ tipo aceitável**</dt> </dl> | Não foi possível encontrar um tipo de mídia aceitável.<br/> |



 

## <a name="remarks"></a>Comentários

Para cada tipo de mídia retornado pela interface **IEnumMediaTypes** , esse método tenta uma conexão chamando o método [**CBasePin:: AttemptConnection**](cbasepin-attemptconnection.md) .

Se o parâmetro *PGTO* for não **nulo**, o PIN ignorará os tipos de mídia que não correspondem a esse tipo. O parâmetro *PGTO* pode especificar um tipo de mídia parcial. Um tipo de mídia parcial tem um valor de GUID \_ NULL para o tipo principal, o subtipo ou o formato. O \_ valor NULL de GUID corresponde a qualquer tipo, semelhante a um valor "curinga".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




