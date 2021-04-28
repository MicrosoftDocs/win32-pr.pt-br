---
description: Construtor de CMsgThread. CMsgThread-método de construtor.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Construtor CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095364"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Construtor CMsgThread. CMsgThread

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMsgThread();
```



## <a name="parameters"></a>Parâmetros

Este construtor não tem parâmetros.

## <a name="remarks"></a>Comentários

A construção de um objeto de thread de mensagem não cria automaticamente o thread. Você deve chamar a função de membro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) para criar o thread.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




