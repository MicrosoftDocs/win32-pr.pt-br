---
description: A função AMovieDllRegisterServer2 registra e cancela o registro de filtros.
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: Função AMovieDllRegisterServer2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec36290b7cad66b2b5f27633d30ae76c3331eba9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748842"
---
# <a name="amoviedllregisterserver2-function"></a>Função AMovieDllRegisterServer2

A função **AMovieDllRegisterServer2** registra e cancela o registro de filtros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bRegister* 
</dt> <dd>

**Verdadeiro** indica registrar o filtro; **falso** indica cancelar o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use essa função para configurar seus filtros. Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dllsetup. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de instalação de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




