---
title: WM_CAP_SET_PREVIEW mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET PREVIEW \_ habilita ou desabilita o modo de visualização.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25bf7f1ce2a61cb104c1e1764f9bca9c82d3aa40d44cc8a1eef9ce435584271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369380"
---
# <a name="wm_cap_set_preview-message"></a>Mensagem WM \_ CAP \_ SET \_ PREVIEW

A **mensagem WM CAP SET \_ \_ \_ PREVIEW** habilita ou desabilita o modo de visualização. No modo de visualização, os quadros são transferidos do hardware de captura para a memória do sistema e exibidos na janela de captura usando funções GDI. Você pode enviar essa mensagem explicitamente ou usando a [**macro capPreview.**](/windows/desktop/api/Vfw/nf-vfw-cappreview)


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Sinalizador de visualização. **Especifique TRUE** para esse parâmetro para habilitar o modo de visualização **ou FALSE** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

O modo de visualização usa recursos substanciais de CPU. Os aplicativos podem desabilitar a visualização ou reduzir a taxa de visualização quando outro aplicativo tem o foco. O **membro fLiveWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de visualização está habilitado no momento.

A habilitação do modo de visualização desabilita automaticamente o modo de sobreposição.

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

 

 





