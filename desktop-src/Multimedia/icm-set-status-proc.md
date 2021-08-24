---
title: ICM_SET_STATUS_PROC mensagem (Vfw.h)
description: A ICM SET STATUS PROC fornece uma função de retorno de \_ chamada de status com o status de uma operação \_ \_ demorada.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678336"
---
# <a name="icm_set_status_proc-message"></a>\_ICM Mensagem SET \_ STATUS \_ PROC

A **ICM SET STATUS \_ \_ \_ PROC** fornece uma função de retorno de chamada de status com o status de uma operação demorada.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Ponteiro para uma [**estrutura ICSETSTATUSPROC.**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamanho, em bytes, de **ICSETSTATUSPROC**.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou se um erro for o contrário.

## <a name="remarks"></a>Comentários

O suporte a essa mensagem é opcional, mas altamente recomendado se a compactação ou descompactação levar mais de um décimo de segundo.

Um aplicativo pode enviar essa mensagem periodicamente para uma função de retorno de chamada de status durante operações demoradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





