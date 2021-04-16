---
description: 'O método QueryId recupera um identificador para o PIN. Esse método implementa o método IPin:: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: Método CTransformInputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daae425e82bbc89cfbc863baea1924e36e63f122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759260"
---
# <a name="ctransforminputpinqueryid-method"></a>Método CTransformInputPin. QueryId

O `QueryId` método recupera um identificador para o PIN. Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Id* 
</dt> <dd>

Recebe uma cadeia de caracteres que contém o identificador do PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Sucesso<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/>       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

O identificador de PIN é usado para persistência de gráfico. O identificador de PIN para esta classe está em. Essa classe substitui o comportamento da classe [**CBasePin**](cbasepin.md) . Na classe **CBasePin** , o identificador de PIN é o mesmo que o nome do PIN, especificado no construtor da classe. Na classe **CTransformInputPin** , o identificador de PIN e o nome do PIN não são iguais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




