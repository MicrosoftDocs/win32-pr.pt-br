---
description: Sinalizador que indica se a qualidade foi alterada.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: Membro CTransformFilter::m_bQualityChanged (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953605"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Membro CTransformFilter::m \_ bQualityChanged

Sinalizador que indica se a qualidade foi alterada. Na primeira vez que o filtro descarta um exemplo, ele envia um evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) para o gerenciador de grafo de filtro e define esse sinalizador como **TRUE.** Ele não envia esse evento novamente até que o filtro seja interrompido e reiniciado, mesmo que ele continue a soltar amostras enquanto isso.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




