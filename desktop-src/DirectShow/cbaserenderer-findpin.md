---
description: O método FindPin recupera o PIN com o identificador especificado.
ms.assetid: d07a298f-ddb0-44eb-85ca-81735875cdf3
title: Método CBaseRenderer. FindPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f639e5d68b11b6a7a65ccfe0d0c6465f822d591b0c4dfd0f4916072fde40856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043766"
---
# <a name="cbaserendererfindpin-method"></a>Método CBaseRenderer. FindPin

O `FindPin` método recupera o PIN com o identificador especificado.

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

Ponteiro para uma constante, Cadeia de caracteres largo terminada em nulo que identifica o PIN. Deve ser L "in".

</dd> <dt>

*ppPin* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN. Se o método falhar, *\* ppPin* será definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                       | Descrição                           |
|---------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl>         | Argumento de ponteiro **nulo** .<br/> |
| <dl> <dt>**VFW \_ E \_ não \_ encontrado**</dt> </dl> | Não encontrado.<br/>                 |



 

## <a name="remarks"></a>Comentários

Esse método substitui o método [**CBaseFilter:: FindPin**](cbasefilter-findpin.md) . O único PIN do filtro (o PIN de entrada) é denominado "in".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




