---
description: Ponteiro para uma estrutura AMOVIESETUP \_ FILTER.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: Membro CFactoryTemplate::m_pAMovieSetup_Filter (Combase.h)
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
ms.openlocfilehash: bc4ee059eb47e08ae827392e8f29968463bb9bd4ca86e0c6b8a87a9f3bbd5667
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697706"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>Membro do filtro CFactoryTemplate::m \_ pAMovieSetup \_

Ponteiro para uma [**estrutura AMOVIESETUP \_ FILTER.**](amoviesetup-filter.md)

## <a name="syntax"></a>Sintaxe


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Comentários

Use essa estrutura para fazer um auto-registro de filtro. Se o componente não for um filtro, essa variável de membro poderá ser **NULL.** Para obter mais informações, consulte How to Register DirectShow Filters.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Combase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




