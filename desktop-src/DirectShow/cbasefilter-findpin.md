---
description: Método CBaseFilter.FindPin – o método FindPin recupera o pino com o identificador especificado. Esse método implementa o método IBaseFilter::FindPin.
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: Método CBaseFilter.FindPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3818ef4356f11a2d003abe4e9442c4de06108aa32e50f480a3d097ea5db0c343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017184"
---
# <a name="cbasefilterfindpin-method"></a>Método CBaseFilter.FindPin

O `FindPin` método recupera o pino com o identificador especificado. Esse método implementa o [**método IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)

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

Ponteiro para uma cadeia de caracteres Unicode com terminação nula constante que identifica o pino.

</dd> <dt>

*ppPin* 
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para a interface [**IPin do**](/windows/desktop/api/Strmif/nn-strmif-ipin) pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT.**



| Código de retorno                                                                                       | Descrição                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Êxito.<br/>                       |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>         | Argumento de ponteiro **NULL.**<br/>     |
| <dl> <dt>**VFW \_ E \_ NÃO \_ ENCONTRADO**</dt> </dl> | Não foi possível encontrar um pino correspondente.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o [**método CBasePin::Name**](cbasepin-name.md) para comparar o nome de cada pino com a cadeia de caracteres especificada pelo *parâmetro Id.*

Se o método for bem-sucedido, a interface **IPin** terá uma contagem de referência pendente. Certifique-se de liberá-lo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




