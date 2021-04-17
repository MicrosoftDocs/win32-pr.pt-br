---
description: Sinalizador que indica se o PIN tenta seus próprios tipos de mídia preferenciais antes daqueles do PIN de recebimento.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754561"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a>Membro de CBasePin:: m \_ bTryMyTypesFirst

Sinalizador que indica se o PIN tenta seus próprios tipos de mídia preferenciais antes daqueles do PIN de recebimento.

## <a name="syntax"></a>Sintaxe


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a>Comentários

Esse sinalizador assume como padrão **false**. Se o sinalizador for **true**, o método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) inverterá a ordem em que ele tenta os tipos de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




