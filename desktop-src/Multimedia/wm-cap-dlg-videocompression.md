---
title: Mensagem de WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION exibe uma caixa de diálogo na qual o usuário pode selecionar um compressor para usar durante o processo de captura.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEOCOMPRESSION
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009337"
---
# <a name="wm_cap_dlg_videocompression-message"></a>Mensagem de VIDEOCOMPRESSION do WM \_ Cap \_ DLG \_

A mensagem do **WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION** exibe uma caixa de diálogo na qual o usuário pode selecionar um compressor para usar durante o processo de captura. A lista de compactadores disponíveis pode variar com o formato de vídeo selecionado na caixa de diálogo formato de vídeo do driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Use esta mensagem com os drivers de captura que fornecem quadros somente no \_ formato RGB de BI. Essa mensagem é mais útil na operação de captura de etapa para combinar a captura e a compactação em uma única operação. A compactação de quadros com um compressor de software como parte de uma operação de captura em tempo real provavelmente é muito demorada.

A compactação não afeta os quadros copiados para a área de transferência.

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

 

 





