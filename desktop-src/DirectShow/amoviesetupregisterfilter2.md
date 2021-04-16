---
description: A função AMovieSetupRegisterFilter2 registra o mérito, os PINs e os tipos de mídia do filtro no registro usando a interface IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Função AMovieSetupRegisterFilter2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750918"
---
# <a name="amoviesetupregisterfilter2-function"></a>Função AMovieSetupRegisterFilter2

A função **AMovieSetupRegisterFilter2** registra o mérito, os PINs e os tipos de mídia do filtro no registro usando a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psetupdata* 
</dt> <dd>

Ponteiro para os dados do [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .

</dd> <dt>

*pIFM2* 
</dt> <dd>

Ponteiro para a interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

</dd> <dt>

*bRegister* 
</dt> <dd>

Valor que indica se o filtro deve ser registrado; **Verdadeiro** indica registrar o filtro; **falso** indica cancelar o registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) chama essa função auxiliar para registrar um filtro após o registro do servidor com.

Normalmente, um filtro usará [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) e não chamará essa função diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dllsetup. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções de instalação de DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




