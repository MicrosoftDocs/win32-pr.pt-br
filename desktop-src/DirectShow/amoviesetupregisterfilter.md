---
description: Obsoleto. Em vez disso, use AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Função AMovieSetupRegisterFilter (Dllsetup.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23f3120bea744303dd95403e8642133de0681dd440c45014f8e787318ab9f857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001871"
---
# <a name="amoviesetupregisterfilter-function"></a>Função AMovieSetupRegisterFilter

Obsoleto. Em vez disso, use [**AMovieSetupRegisterFilter2.**](amoviesetupregisterfilter2.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psetupdata* 
</dt> <dd>

Reservado.

</dd> <dt>

*pIFM* 
</dt> <dd>

Reservado.

</dd> <dt>

*Bregister* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dllsetup.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de instalação de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




