---
title: Mensagem de WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: A \_ mensagem de \_ erro definir retorno de chamada do WM Cap \_ \_ define uma função de retorno de chamada de erro no aplicativo cliente. AVICap chama esse procedimento quando ocorrem erros. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_ERROR
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455323"
---
# <a name="wm_cap_set_callback_error-message"></a>\_Mensagem de \_ erro de retorno de chamada de Set Cap do \_ WM \_

A mensagem de **\_ \_ \_ \_ erro definir retorno de chamada do WM Cap** define uma função de retorno de chamada de erro no aplicativo cliente. AVICap chama esse procedimento quando ocorrem erros. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada de erro, do tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Especifique **NULL** para este parâmetro para desabilitar uma função de retorno de chamada de erro anteriormente instalada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Os aplicativos podem, opcionalmente, definir uma função de retorno de chamada de erro. Se definido, AVICap chamará o procedimento de erro nas seguintes situações:

-   O disco está cheio.
-   Uma janela de captura não pode ser conectada a um driver de captura.
-   Um dispositivo de formato de onda-áudio não pode ser aberto.
-   O número de quadros removidos durante a captura excede o percentual especificado.
-   Os quadros não podem ser capturados devido a problemas de interrupção de sincronização vertical.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





