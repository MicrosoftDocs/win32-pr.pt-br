---
description: Uma função de retorno de chamada usada para notificar o host do progresso dos mecanismos. Isso também serve como uma maneira para o host determinar que o mecanismo ainda está em execução.
title: 'Método IStatusCallback:: status'
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
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812339"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Método IStatusCallback:: status

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
O tempo decorrido desde a última chamada para status, em milissegundos.

*dwFramesCaptured*   
O número de quadros que foram capturados desde a última chamada para o status.

*dwFramesElapsed*   
O número de quadros decorridos desde a última chamada para o status.

## <a name="return-value"></a>Retornar valor

Se esse método tiver sucesso, ele retornará **S_OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>parâmetro</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
