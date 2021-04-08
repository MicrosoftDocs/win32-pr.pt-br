---
title: Mensagem de WM_CAP_SET_PREVIEWRATE (VFW. h)
description: A mensagem do conjunto de Cap do WM \_ \_ \_ PREVIEWRATE define a taxa de exibição do quadro no modo de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_PREVIEWRATE
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919115"
---
# <a name="wm_cap_set_previewrate-message"></a>\_Mensagem de \_ PREVIEWRATE do conjunto de Cap do WM \_

A mensagem do **conjunto de Cap do WM \_ \_ \_ PREVIEWRATE** define a taxa de exibição do quadro no modo de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*
</dt> <dd>

Taxa, em milissegundos, na qual novos quadros são capturados e exibidos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

O modo de visualização usa recursos de CPU substanciais. Os aplicativos podem desabilitar a visualização ou diminuir a taxa de visualização quando outro aplicativo tiver o foco. Durante a captura de vídeo de streaming, a tarefa de visualização é a prioridade mais baixa do que a gravação de quadros em disco, e os quadros de versão prévia serão exibidos somente se nenhum outro buffer estiver disponível para gravação.

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

 

 





