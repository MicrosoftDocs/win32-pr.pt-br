---
description: Função AMovieDllUnregisterServer – obsoleta. Use AMovieDllRegisterServer2 em vez disso.
ms.assetid: 80f52109-6239-4e3d-a395-eb69f5278cd2
title: Função AMovieDllUnregisterServer (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllUnregisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df7fb34246249298efc143b7ccc8e6332540867c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099924"
---
# <a name="amoviedllunregisterserver-function"></a>Função AMovieDllUnregisterServer

Obsoleto. Use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) em vez disso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AMovieDllUnregisterServer(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dllsetup. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Funções de instalação de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




