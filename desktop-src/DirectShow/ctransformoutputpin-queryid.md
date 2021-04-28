---
description: 'Método CTransformOutputPin. QueryId – o método QueryId recupera um identificador para o PIN. Esse método implementa o método IPin:: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Método CTransformOutputPin. QueryId (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094844"
---
# <a name="ctransformoutputpinqueryid-method"></a>Método CTransformOutputPin. QueryId

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

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/>       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

O identificador de PIN é usado para persistência de gráfico. O identificador de PIN para esta classe está fora. Essa classe substitui o comportamento da classe [**CBasePin**](cbasepin.md) . Na classe **CBasePin** , o identificador de PIN é o mesmo que o nome do PIN, especificado no construtor da classe. Na classe **CTransformInputPin** , o identificador de PIN e o nome do PIN não são iguais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




