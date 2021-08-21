---
title: WM_CAP_SET_PREVIEWRATE mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ PREVIEWRATE define a taxa de exibição do quadro no modo de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE mensagem Windows Multimídia
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
ms.openlocfilehash: fa9b9a24614a40c5efb545b91a80069bf915c77c4b7d8fb289ed581f750ac0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135078"
---
# <a name="wm_cap_set_previewrate-message"></a>Mensagem WM \_ CAP \_ SET \_ PREVIEWRATE

A **mensagem WM CAP SET \_ \_ \_ PREVIEWRATE** define a taxa de exibição do quadro no modo de visualização. Você pode enviar essa mensagem explicitamente ou usando a [**macro capPreviewRate.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate)


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*Wms*
</dt> <dd>

Taxa, em milissegundos, na qual novos quadros são capturados e exibidos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

O modo de visualização usa recursos substanciais de CPU. Os aplicativos podem desabilitar a visualização ou reduzir a taxa de visualização quando outro aplicativo tem o foco. Durante a captura de vídeo de streaming, a tarefa de visualização é mais baixa do que a gravação de quadros no disco e os quadros de visualização são exibidos somente se nenhum outro buffer estiver disponível para gravação.

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

 

 





