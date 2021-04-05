---
title: Mensagem de WM_CAP_SET_PREVIEW (VFW. h)
description: A mensagem de visualização do conjunto de Cap do WM \_ \_ \_ habilita ou desabilita o modo de visualização.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_PREVIEW
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
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086367"
---
# <a name="wm_cap_set_preview-message"></a>\_Mensagem de \_ visualização do conjunto de Cap do WM \_

A mensagem de visualização do conjunto de Cap do WM habilita ou desabilita o modo de visualização. **\_ \_ \_** No modo de visualização, os quadros são transferidos do hardware de captura para a memória do sistema e, em seguida, exibidos na janela de captura usando funções GDI. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*fixo*
</dt> <dd>

Sinalizador de visualização. Especifique **true** para esse parâmetro para habilitar o modo de visualização ou **false** para desabilitá-lo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O modo de visualização usa recursos de CPU substanciais. Os aplicativos podem desabilitar a visualização ou diminuir a taxa de visualização quando outro aplicativo tiver o foco. O membro **fLiveWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de visualização está habilitado no momento.

Habilitar o modo de visualização desabilita automaticamente o modo de sobreposição.

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

 

 





