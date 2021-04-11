---
title: Mensagem de WM_CAP_SET_SCALE (VFW. h)
description: A \_ \_ \_ mensagem definir escala do WM Cap habilita ou desabilita o dimensionamento das imagens de vídeo de visualização.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_SCALE
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
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086366"
---
# <a name="wm_cap_set_scale-message"></a>\_Mensagem de \_ escala do conjunto de Cap do WM \_

A **mensagem \_ \_ definir \_ escala do WM Cap** habilita ou desabilita o dimensionamento das imagens de vídeo de visualização. Se a colocação em escala estiver habilitada, o quadro de vídeo capturado será alongado para as dimensões da janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="f"></span><span id="F"></span>*fixo*
</dt> <dd>

Sinalizador de escala de visualização. Especifique **true** para esse parâmetro para alongar os quadros de visualização para o tamanho da janela de captura ou **false** para exibi-los em seu tamanho natural.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Dimensionar imagens de visualização controla a apresentação imediata de quadros capturados dentro da janela de captura. Ele não tem nenhum efeito sobre o tamanho dos quadros salvos no arquivo.

O dimensionamento não tem nenhum efeito ao usar a sobreposição para exibir o vídeo no buffer de quadros.

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

 

 





