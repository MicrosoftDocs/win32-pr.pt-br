---
title: WM_CAP_GET_STATUS mensagem (Vfw.h)
description: A mensagem WM \_ CAP GET STATUS recupera o status da janela de \_ \_ captura. Você pode enviar essa mensagem explicitamente ou usando a macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805befc3f83c79b157e040004dcf382dccaf07b240b3b846892b8fb035f826ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135152"
---
# <a name="wm_cap_get_status-message"></a>Mensagem WM \_ CAP \_ GET \_ STATUS

A **mensagem WM CAP GET \_ \_ \_ STATUS** recupera o status da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a [**macro capGetStatus.**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus)


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*Wsize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*s*
</dt> <dd>

Ponteiro para uma [**estrutura CAPSTATUS.**](/windows/win32/api/vfw/ns-vfw-capstatus)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

A [**estrutura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contém o estado atual da janela de captura. Como esse estado é dinâmico e muda em resposta a várias mensagens, o aplicativo deve inicializar essa estrutura depois de enviar a mensagem [**WM \_ CAP \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou usando a [**macro capDlgVideoFormat)**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) e sempre que precisar habilitar itens de menu ou determinar o estado real da janela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





