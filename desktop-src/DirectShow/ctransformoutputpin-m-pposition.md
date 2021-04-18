---
description: Objeto auxiliar para passar comandos de busca upstream.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membro CTransformOutputPin:: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749824"
---
# <a name="ctransformoutputpinm_pposition-member"></a>Membro de CTransformOutputPin:: m \_ pPosition

Objeto auxiliar para passar comandos de busca upstream.

## <a name="syntax"></a>Sintaxe


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Comentários

Quando o PIN é consultado pela primeira vez para a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , ele cria e agrega um objeto auxiliar [**CPosPassThru**](cpospassthru.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




