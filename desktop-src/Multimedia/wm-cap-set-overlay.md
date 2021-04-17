---
title: Mensagem de WM_CAP_SET_OVERLAY (VFW. h)
description: A \_ mensagem de sobreposição do conjunto de Cap do WM \_ \_ habilita ou desabilita o modo de sobreposição. No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware. Você pode enviar essa mensagem explicitamente ou usando a macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_OVERLAY
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812897"
---
# <a name="wm_cap_set_overlay-message"></a>\_Mensagem de \_ sobreposição do conjunto de Cap do WM \_

A mensagem de **\_ \_ \_ sobreposição do conjunto de Cap do WM** habilita ou desabilita o modo de sobreposição. No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware. Você pode enviar essa mensagem explicitamente ou usando a macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*fixo*
</dt> <dd>

Sinalizador de sobreposição. Especifique **true** para esse parâmetro para habilitar o modo de sobreposição ou **false** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O uso de uma sobreposição não exige recursos de CPU.

O membro **fHasOverlay** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se o dispositivo é capaz de sobrepor. O membro **fOverlayWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de sobreposição está habilitado no momento.

Habilitar o modo de sobreposição desabilita automaticamente o modo de visualização.

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

 

 





