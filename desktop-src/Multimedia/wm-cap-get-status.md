---
title: Mensagem de WM_CAP_GET_STATUS (VFW. h)
description: A \_ mensagem de status obter do WM Cap \_ \_ recupera o status da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capGetStatus.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_STATUS
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
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008830"
---
# <a name="wm_cap_get_status-message"></a>\_Mensagem de \_ status de obtenção de Cap do WM \_

A mensagem de **\_ \_ \_ status obter do WM Cap** recupera o status da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) .


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*&*
</dt> <dd>

Ponteiro para uma estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

A estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) contém o estado atual da janela de captura. Como esse estado é dinâmico e muda em resposta a várias mensagens, o aplicativo deve inicializar essa estrutura após enviar a mensagem de [**VIDEOFORMAT do WM \_ Cap \_ DLG \_**](wm-cap-dlg-videoformat.md) (ou usar a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ) e sempre que precisar habilitar itens de menu ou determinar o estado real da janela.

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

 

 





