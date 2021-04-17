---
description: 'Sinalizador que indica se o retorno de chamada de versão está habilitado. Esse sinalizador é definido no método do construtor. Se o valor for FALSE, chamar o método CBaseAllocator:: setnotificar fará com que uma asserção seja acionada (em compilações de depuração).'
ms.assetid: cc9adc7c-ec44-41e7-875a-b3e553120804
title: 'Membro CBaseAllocator:: m_fEnableReleaseCallback (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fEnableReleaseCallback
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 626f1e8f4101eb48e79bc1cf679d1b91be9b2b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768409"
---
# <a name="cbaseallocatorm_fenablereleasecallback-member"></a>Membro de CBaseAllocator:: m \_ fEnableReleaseCallback

Sinalizador que indica se o retorno de chamada de versão está habilitado. Esse sinalizador é definido no método do construtor. Se o valor for **false**, chamar o método [**CBaseAllocator:: setnotificar**](cbaseallocator-setnotify.md) fará com que uma asserção seja acionada (em compilações de depuração).

## <a name="syntax"></a>Syntax


```C++
BOOL m_fEnableReleaseCallback;
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

 

 




