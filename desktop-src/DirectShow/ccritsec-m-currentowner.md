---
description: Identificador de thread do thread proprietário.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membro CCritSec:: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748206"
---
# <a name="ccritsecm_currentowner-member"></a>Membro de CCritSec:: m \_ currentOwner

Identificador de thread do thread proprietário.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Comentários

Essa variável de membro é definida somente na versão de depuração da classe base. A [seção crítica Depurando funções](critical-section-debugging-functions.md) usa esse membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




