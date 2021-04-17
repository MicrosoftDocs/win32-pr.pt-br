---
description: 'O método FindPin Obtém o PIN com o identificador especificado. Esse método implementa o método IBaseFilter:: FindPin.'
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: Método CTransformFilter. FindPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747809"
---
# <a name="ctransformfilterfindpin-method"></a>Método CTransformFilter. FindPin

O método **FindPin** Obtém o PIN com o identificador especificado. Esse método implementa o método [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Id* 
</dt> <dd>

Cadeia de caracteres largos que contém o identificador do PIN.

</dd> <dt>

*ppPin* 
</dt> <dd>

Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN. Se o método falhar, `*ppPin` será definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memória insuficiente.<br/>                       |
| <dl> <dt>**\_ponteiro E**</dt> </dl>         | Argumento de ponteiro **nulo** .<br/>                 |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | Não foi possível encontrar um PIN com este identificador.<br/> |



 

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> A implementação desse método não chama [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) para corresponder ao identificador do PIN. Em vez disso, o método pressupõe que o pino de entrada é denominado "in", e o pino de saída é chamado de "out". Se você usar um conjunto diferente de identificadores de PIN, substitua esse método.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




