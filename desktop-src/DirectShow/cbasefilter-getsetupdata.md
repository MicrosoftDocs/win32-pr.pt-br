---
description: O método GetSetupData recupera os dados de registro do filtro.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Método CBaseFilter.GetSetupData (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f86bc35688ab0ec1c19053a95cbfd2025cf45ad666ef419fdb8440c6a844cb61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640466"
---
# <a name="cbasefiltergetsetupdata-method"></a>Método CBaseFilter.GetSetupData

O `GetSetupData` método recupera os dados de registro para o filtro.

> [!Note]  
> Esse método é obsoleto. Ele é chamado pelos [**métodos CBaseFilter::Register**](cbasefilter-register.md) e [**CBaseFilter::Unregister.**](cbasefilter-unregister.md)

 

## <a name="syntax"></a>Sintaxe


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um ponteiro para uma estrutura [**AMOVIESETUP \_ FILTER**](amoviesetup-filter.md) que contém informações de registro para o filtro.

## <a name="remarks"></a>Comentários

A classe base retorna **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




