---
description: Sinalizador que indica se a qualidade foi alterada.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Membro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
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
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759263"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Membro de CTransformFilter:: m \_ bQualityChanged

Sinalizador que indica se a qualidade foi alterada. Na primeira vez que o filtro descartar um exemplo, ele enviará um evento de [**\_ \_ alteração de qualidade do EC**](ec-quality-change.md) para o Gerenciador do grafo de filtro e definirá esse sinalizador como **true**. Ele não envia esse evento novamente até que o filtro seja interrompido e reiniciado, mesmo que ele continue a descartar amostras enquanto isso.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




