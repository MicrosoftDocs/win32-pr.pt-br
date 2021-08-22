---
description: O método cancelar registro remove o filtro do registro.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Método CBaseFilter. Unregister (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317896"
---
# <a name="cbasefilterunregister-method"></a>Método CBaseFilter. Unregister

O `Unregister` método remove o filtro do registro.

> [!Note]  
> Esse método é obsoleto. Novos filtros devem ter o registro cancelado usando a função [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) . para obter mais informações, consulte [como registrar filtros de DirectShow](how-to-register-directshow-filters.md).

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




