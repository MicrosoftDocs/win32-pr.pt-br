---
description: O método Register adiciona o filtro ao registro.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Método CBaseFilter. Register (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168d84d3bfc90fb710ae65a3b887eeb5575db407361a256c48161f0f7968a53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403519"
---
# <a name="cbasefilterregister-method"></a>Método CBaseFilter. Register

O `Register` método adiciona o filtro ao registro.

> [!Note]  
> Esse método é obsoleto. Novos filtros devem ser registrados usando a função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . para obter mais informações, consulte [como registrar filtros de DirectShow](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Register();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                  |
| <dl> <dt>**\_falso**</dt> </dl> | Não há informações de registro disponíveis.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




