---
description: 'Método CBasePin. EnumMediaTypes – o método EnumMediaTypes enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método IPin:: EnumMediaTypes.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Método CBasePin. EnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95c79071030b2f40613138e526abd1f965d3b5aeb7b233c2c53be57b65f97da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916396"
---
# <a name="cbasepinenummediatypes-method"></a>Método CBasePin. EnumMediaTypes

O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                   | Descrição                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo** .<br/> |



 

## <a name="remarks"></a>Comentários

Os Pins de entrada não são necessários para enumerar os tipos preferenciais. Os Pins de saída devem enumerar pelo menos um tipo preferencial. Caso contrário, ambos os Pins podem não ter um tipo preferencial, tornando impossível uma conexão.

A interface **IEnumMediaTypes** funciona como um enumerador com padrão. Para obter mais informações, consulte [Enumerando objetos em um filtro Graph](enumerating-objects-in-a-filter-graph.md). Se o método tiver sucesso, a interface **IEnumMediaTypes** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

A classe base [**CEnumMediaTypes**](cenummediatypes.md) implementa **IEnumMediaTypes**. Ele chama o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) do PIN para enumerar os tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




