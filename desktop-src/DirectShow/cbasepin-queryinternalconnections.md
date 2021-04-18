---
description: 'O método QueryInternalConnections recupera os PINs que estão conectados internamente a esse PIN (dentro do filtro). Esse método implementa o método IPin:: QueryInternalConnections.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Método CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752902"
---
# <a name="cbasepinqueryinternalconnections-method"></a>Método CBasePin. QueryInternalConnections

O `QueryInternalConnections` método recupera os PINs que estão conectados internamente a esse PIN (dentro do filtro). Esse método implementa o método [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*apPin* 
</dt> <dd>

Endereço de uma matriz de ponteiros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*nPin* 
</dt> <dd>

Em entrada, especifica o tamanho da matriz. Quando o método retorna, o valor é definido como o número de ponteiros retornados na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | Tamanho de matriz insuficiente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                 |
| <dl> <dt>**E \_ falha**</dt> </dl>    | Falha.<br/>                 |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Não implementado.<br/>         |



 

## <a name="remarks"></a>Comentários

Em alguns filtros, os Pins de entrada correspondem a Pins de saída específicos. Para cada PIN, esse método preenche uma matriz com ponteiros para os Pins correspondentes. Se cada PIN de entrada fornecer dados para cada pino de saída, retornará E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




