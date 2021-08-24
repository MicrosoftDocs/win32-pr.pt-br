---
title: WM_CAP_SET_SCROLL mensagem (Vfw.h)
description: A mensagem WM \_ CAP SET SCROLL define a parte do quadro de vídeo a ser exibida na janela de \_ \_ captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 352d65c2ad8e80622f7ff50cca0a8f7d6e523d53ae002a2325327a634b97c931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134980"
---
# <a name="wm_cap_set_scroll-message"></a>Mensagem WM \_ CAP \_ SET \_ SCROLL

A **mensagem WM CAP SET \_ \_ \_ SCROLL** define a parte do quadro de vídeo a ser exibida na janela de captura. Essa mensagem define o canto superior esquerdo da área do cliente da janela de captura para as coordenadas de um pixel especificado dentro do quadro de vídeo. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetScrollPos.**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos)


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*Lpp*
</dt> <dd>

Endereço para conter a posição de rolagem desejada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

A posição de rolagem afeta a imagem nos modos de visualização e sobreposição.

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

 

 





