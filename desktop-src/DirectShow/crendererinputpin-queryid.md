---
description: O método QueryId recupera o identificador de pino. Esse método substitui o método CBasePin::QueryId.
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: Método CRendererInputPin.QueryId (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 732bf7aa6d0d247c93c0334db48b86bccd2ac15715dd2da9a4d60a0d315966bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054567"
---
# <a name="crendererinputpinqueryid-method"></a>Método CRendererInputPin.QueryId

O `QueryId` método recupera o identificador de pino. Esse método substitui o [**método CBasePin::QueryId.**](cbasepin-queryid.md)

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

Recebe uma cadeia de caracteres que contém o identificador de pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                   | Descrição                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente<br/>       |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | **Argumento de** ponteiro NULL<br/> |



 

## <a name="remarks"></a>Comentários

Esse método aloca a cadeia de caracteres largos "In" e a atribui ao *parâmetro Id.* O chamador deve liberar a memória alocada usando a **função CoTaskMemFree.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 




