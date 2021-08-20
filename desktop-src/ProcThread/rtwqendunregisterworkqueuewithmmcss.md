---
description: Conclui uma solicitação assíncrona para o registro de uma fila de trabalho com uma tarefa MMCSS (Serviço de Agendador de Classes Multimídia).
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
ms.openlocfilehash: 083f0ca787bb842850320b9dd1d320ef4d5b172ee0b6d9b117296e58b991bd0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793396"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a>Função RtwqEndUnregisterWorkQueueWithMMCSS

Conclui uma solicitação assíncrona para o registro de uma fila de trabalho com uma tarefa MMCSS (Serviço de Agendador de Classes Multimídia).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Presult* 
</dt> <dd>

Ponteiro para a interface [**IMFAsyncResult.**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) Passe o mesmo ponteiro recebido pelo objeto de retorno de chamada [**no método IRtwqAsyncCallback::Invoke.**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem-sucedida, ela retornará **S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Nenhum</dt> </dl>        |
| Biblioteca<br/>                  | <dl> <dt>Rtworkq.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RTWorkQ.dll</dt> </dl> |



 

 
