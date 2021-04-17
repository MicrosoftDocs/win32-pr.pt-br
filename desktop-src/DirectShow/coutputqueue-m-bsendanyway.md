---
description: 'Sinalizador para substituir o processamento em lotes. Definir esse sinalizador como TRUE substitui o sinalizador COutputQueue:: m \_ bBatchExact e entrega todas as amostras pendentes.'
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'Membro COutputQueue:: m_bSendAnyway (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755586"
---
# <a name="coutputqueuem_bsendanyway-member"></a>Membro de COutputQueue:: m \_ bSendAnyway

Sinalizador para substituir o processamento em lotes. Definir esse sinalizador como **true** substitui o sinalizador [**COutputQueue:: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) e entrega todas as amostras pendentes.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bSendAnyway;
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

 

 




