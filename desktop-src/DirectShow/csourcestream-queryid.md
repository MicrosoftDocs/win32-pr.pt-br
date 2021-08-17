---
description: O método QueryId recupera um identificador para o PIN.
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: Método CSourceStream. QueryId (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd8582d16022c9d5dfd60eb87847d564ef69203e329ff37eaa9c2964a11794c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317506"
---
# <a name="csourcestreamqueryid-method"></a>Método CSourceStream. QueryId

O `QueryId` método recupera um identificador para o PIN.

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

Ponteiro para uma variável que recebe uma cadeia de caracteres que contém o identificador do PIN.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memória insuficiente.<br/>             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>         | Argumento de ponteiro **nulo** .<br/>       |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | O PIN não foi encontrado no filtro.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método implementa o método [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) . Para construir uma cadeia de caracteres de identificador, o PIN chama o método [**CSource:: FindPinNumber**](csource-findpinnumber.md) como o parâmetro. O método **FindPinNumber** retorna o número do PIN, indexado de zero. `QueryId` incrementa o valor de retorno em um e converte o resultado em uma cadeia de caracteres. Por exemplo, o primeiro PIN se torna "1"; o segundo PIN se torna "2"; e assim por diante.

Se esse método retornar VFW \_ e \_ não \_ for encontrado, ele indicará que a matriz de Pins do filtro é inválida, supostamente causada por um bug no filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




