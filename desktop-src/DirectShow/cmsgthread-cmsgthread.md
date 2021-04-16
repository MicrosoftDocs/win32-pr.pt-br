---
description: Método de construtor.
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
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758543"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




