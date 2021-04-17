---
description: Fila de exemplo de mídia.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Membro COutputQueue:: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768658"
---
# <a name="coutputqueuem_list-member"></a>Membro da lista COutputQueue:: m \_

Fila de exemplo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é um ponteiro para um objeto [**CGenericList**](cgenericlist.md) que mantém ponteiros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . O tipo **CSampleList** é definido da seguinte maneira:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




