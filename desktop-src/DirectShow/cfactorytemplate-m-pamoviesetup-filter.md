---
description: Ponteiro para uma \_ estrutura de filtro AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Membro CFactoryTemplate:: m_pAMovieSetup_Filter (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769219"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>Membro de filtro CFactoryTemplate:: m \_ pAMovieSetup \_

Ponteiro para uma estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .

## <a name="syntax"></a>Sintaxe


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Comentários

Use essa estrutura para fazer um filtro se registrar automaticamente. Se o componente não for um filtro, essa variável de membro poderá ser **nula**. Para obter mais informações, consulte como registrar filtros do DirectShow.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




