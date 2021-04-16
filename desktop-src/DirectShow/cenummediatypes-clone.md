---
description: 'O método clone faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o método IEnumMediaTypes:: clone.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Método CEnumMediaTypes. Clone (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750483"
---
# <a name="cenummediatypesclone-method"></a>Método CEnumMediaTypes. Clone

O `Clone` método faz uma cópia do enumerador com o mesmo estado de enumeração. Esse método implementa o método [**IEnumMediaTypes:: clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) do novo enumerador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Memória insuficiente.<br/>                                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                  | Argumento de ponteiro **nulo** .<br/>                                               |
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

 

 




