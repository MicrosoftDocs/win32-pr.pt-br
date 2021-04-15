---
title: Mensagem de ICM_SET_STATUS_PROC (VFW. h)
description: A \_ mensagem ICM Set \_ status \_ proc fornece uma função de retorno de chamada de status com o status de uma operação demorada.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- Multimídia do Windows de mensagem ICM_SET_STATUS_PROC
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
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456037"
---
# <a name="icm_set_status_proc-message"></a>\_Mensagem de \_ procedimento de status de configuração ICM \_

A mensagem **ICM \_ set \_ status \_ proc** fornece uma função de retorno de chamada de status com o status de uma operação demorada.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Ponteiro para uma estrutura [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de **ICSETSTATUSPROC**.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O suporte a essa mensagem é opcional, mas é altamente recomendável se a compactação ou descompactação demorar mais do que aproximadamente um décimo de segundo.

Um aplicativo pode enviar essa mensagem periodicamente para uma função de retorno de chamada de status durante operações demoradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





