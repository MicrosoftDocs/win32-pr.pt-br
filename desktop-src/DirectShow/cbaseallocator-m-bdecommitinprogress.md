---
description: Sinalizador que indica se uma operação de desconfirmação está em andamento.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Membro CBaseAllocator:: m_bDecommitInProgress (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755367"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Membro de CBaseAllocator:: m \_ bDecommitInProgress

Sinalizador que indica se uma operação de desconfirmação está em andamento. O valor é **true** após o método [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) ser chamado, mas antes de todos os buffers terem sido liberados. Se o valor for **true**, o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) falhará. Além disso, o alocador não deve ser excluído a si mesmo enquanto o valor é **true**.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




