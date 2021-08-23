---
description: Usa a função Microsoft Win32 SetThreadPriority para definir a prioridade do thread para um novo valor.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Método CMsgThread.SetThreadPriority (Msgthrd.h)
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
ms.openlocfilehash: ce293f32f765a89451ecf07b4532afc5fc4a7a132287d5b09b54962f93135215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585666"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>Método CMsgThread.SetThreadPriority

Usa a função Microsoft Win32 **SetThreadPriority** para definir a prioridade do thread para um novo valor.

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

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                              | Descrição                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE****</dt> </dl>  | A prioridade foi definida com êxito.<br/> |
| <dl> <dt>FALSE****</dt> </dl> | A prioridade não foi definida.<br/>          |



 

## <a name="remarks"></a>Comentários

O cliente e o thread de trabalho podem chamar essa função de membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




