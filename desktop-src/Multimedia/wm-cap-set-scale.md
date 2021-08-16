---
title: WM_CAP_SET_SCALE mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET SCALE \_ habilita ou desabilita o dimensionamento das imagens de vídeo de visualização.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293be6917917581957df0f5dae9456274f1d2cc3eeffff5ea971c3596209a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369390"
---
# <a name="wm_cap_set_scale-message"></a>Mensagem WM \_ CAP \_ SET \_ SCALE

A **mensagem WM CAP SET \_ \_ \_ SCALE** habilita ou desabilita o dimensionamento das imagens de vídeo de visualização. Se o dimensionamento estiver habilitado, o quadro de vídeo capturado será estendido para as dimensões da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a [**macro capPreviewScale.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale)


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Sinalizador de dimensionamento de visualização. **Especifique TRUE** para esse parâmetro alongar quadros de visualização para o tamanho da janela de captura ou **FALSE** para exibi-los em seu tamanho natural.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

O dimensionamento de imagens de visualização controla a apresentação imediata de quadros capturados dentro da janela de captura. Ele não tem efeito sobre o tamanho dos quadros salvos no arquivo.

O dimensionamento não tem nenhum efeito ao usar a sobreposição para exibir vídeo no buffer de quadro.

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

 

 





