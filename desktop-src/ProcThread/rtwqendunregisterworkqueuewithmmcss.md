---
description: Conclui uma solicitação assíncrona para cancelar o registro de uma fila de trabalho com uma tarefa do serviço de Agendador de classes de multimídia (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Função RtwqEndUnregisterWorkQueueWithMMCSS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828698"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Função RtwqEndUnregisterWorkQueueWithMMCSS

Conclui uma solicitação assíncrona para cancelar o registro de uma fila de trabalho com uma tarefa do serviço de Agendador de classes de multimídia (MMCSS).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pResult* 
</dt> <dd>

Ponteiro para a interface [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) . Passe o mesmo ponteiro que o seu objeto de retorno de chamada recebeu no método [**IRtwqAsyncCallback:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Nenhuma</dt> </dl>        |
| Biblioteca<br/>                  | <dl> <dt>Rtworkq. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
