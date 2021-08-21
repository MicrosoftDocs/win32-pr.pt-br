---
title: WM_CAP_SET_OVERLAY mensagem (Vfw.h)
description: A mensagem OVERLAY WM \_ CAP \_ SET \_ habilita ou desabilita o modo de sobreposição. No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware. Você pode enviar essa mensagem explicitamente ou usando a macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY mensagem Windows Multimídia
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
ms.openlocfilehash: 10f2161f3c163fb5f6c411293770a2b2ba3907bef7eb03aad2d67b0e0637abbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135088"
---
# <a name="wm_cap_set_overlay-message"></a>Mensagem WM \_ CAP \_ SET \_ OVERLAY

A **mensagem \_ \_ \_ OVERLAY WM CAP SET** habilita ou desabilita o modo de sobreposição. No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware. Você pode enviar essa mensagem explicitamente ou usando a [**macro capOverlay.**](/windows/desktop/api/Vfw/nf-vfw-capoverlay)


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Sinalizador de sobreposição. **Especifique TRUE** para esse parâmetro para habilitar o modo de sobreposição **ou FALSE** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

O uso de uma sobreposição não requer recursos de CPU.

O **membro fHasOverlay** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se o dispositivo é capaz de sobrepor. O **membro fOverlayWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de sobreposição está habilitado no momento.

A habilitação do modo de sobreposição desabilita automaticamente o modo de visualização.

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

 

 





