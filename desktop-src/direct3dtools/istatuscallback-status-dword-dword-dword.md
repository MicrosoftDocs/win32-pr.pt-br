---
description: Uma função de retorno de chamada usada para notificar o host do progresso dos mecanismos. Isso também serve como uma maneira para o host determinar que o mecanismo ainda está em execução.
title: Método IStatusCallback::Status
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622302"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Método IStatusCallback::Status

Uma função de retorno de chamada usada para notificar o host do progresso do mecanismo. Isso também serve como uma maneira para o host determinar que o mecanismo ainda está em execução.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Parâmetros

*dwMillisecondsElapsed*   
O tempo decorrido desde a última chamada para Status, em milissegundos.

*dwFramesCaptured*   
O número de quadros que foram capturados desde a última chamada para Status.

*dwFramesElapsed*   
O número de quadros decorridos desde a última chamada para Status.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S_OK**. Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
