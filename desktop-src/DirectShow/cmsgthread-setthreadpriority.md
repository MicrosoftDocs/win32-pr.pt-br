---
description: Usa a função SetThreadPriority do Microsoft Win32 para definir a prioridade do thread para um novo valor.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Método CMsgThread. SetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754533"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>Método CMsgThread. SetThreadPriority

Usa a função **SetThreadPriority** do Microsoft Win32 para definir a prioridade do thread para um novo valor.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nPriority* 
</dt> <dd>

Prioridade do thread.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                              | Descrição                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>VERDADEIRO * * * *</dt> </dl>  | A prioridade foi definida com êxito.<br/> |
| <dl> <dt>FALSE * * * *</dt> </dl> | A prioridade não foi definida.<br/>          |



 

## <a name="remarks"></a>Comentários

O cliente e o thread de trabalho podem chamar essa função de membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




