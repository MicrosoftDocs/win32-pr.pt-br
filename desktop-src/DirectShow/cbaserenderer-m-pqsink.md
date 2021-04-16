---
description: Ponteiro para o objeto que recebe mensagens de controle de qualidade.
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: 'Membro CBaseRenderer:: m_pQSink (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 331504ffaeb74d84382b65d1332f6dbe7c9556dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750487"
---
# <a name="cbaserendererm_pqsink-member"></a>Membro de CBaseRenderer:: m \_ pQSink

Ponteiro para o objeto que recebe mensagens de controle de qualidade.

## <a name="syntax"></a>Sintaxe


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a>Comentários

A classe base não implementa o controle de qualidade. Essa variável de membro usa como padrão **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




