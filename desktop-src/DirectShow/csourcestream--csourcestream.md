---
description: CSourceStream. ~ CSourceStream destruidor-método Destruitor.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Destruidor CSourceStream. ~ CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085204"
---
# <a name="csourcestreamcsourcestream-destructor"></a>Destruidor CSourceStream. ~ CSourceStream

Método destruidor.

## <a name="syntax"></a>Sintaxe


```C++
~CSourceStream();
```



## <a name="remarks"></a>Comentários

O destruidor remove automaticamente o PIN do filtro proprietário, chamando [**CSource:: RemovePin**](csource-removepin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Source. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




