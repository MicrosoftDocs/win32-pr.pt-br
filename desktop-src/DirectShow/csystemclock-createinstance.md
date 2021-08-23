---
description: O método CreateInstance cria uma nova instância desse objeto .
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Método CSystemClock.CreateInstance (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63626804ad4d067e5067170e0fc17cc83c179a906c0e625bb02a3ffb8a4ef197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687326"
---
# <a name="csystemclockcreateinstance-method"></a>Método CSystemClock.CreateInstance

O `CreateInstance` método cria uma nova instância desse objeto .

## <a name="syntax"></a>Sintaxe


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Punk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de agreging.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma nova instância desse objeto.

## <a name="remarks"></a>Comentários

A fábrica de classes chama esse método para criar o objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Sysclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




