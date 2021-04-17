---
description: 'O método Skip ignora um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes:: Skip.'
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Método CEnumMediaTypes. Skip (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e09217bc45b866cfb08aa2ab0cae5a7a28815fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748205"
---
# <a name="cenummediatypesskip-method"></a>Método CEnumMediaTypes. Skip

O `Skip` método ignora um número especificado de tipos de mídia. Esse método implementa o método [**IEnumMediaTypes:: Skip**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Número de tipos de mídia a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                    | Ignorado após o fim da sequência.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt> </dl> | O estado do PIN foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




