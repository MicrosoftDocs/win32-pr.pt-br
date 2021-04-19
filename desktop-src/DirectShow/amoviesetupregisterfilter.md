---
description: Obsoleto. Use AMovieSetupRegisterFilter2 em vez disso.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Função AMovieSetupRegisterFilter (Dllsetup. h)
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
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785506"
---
# <a name="amoviesetupregisterfilter-function"></a>Função AMovieSetupRegisterFilter

Obsoleto. Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) em vez disso.

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

*bRegister* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dllsetup. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de instalação de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




