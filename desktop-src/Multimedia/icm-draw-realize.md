---
title: Mensagem de ICM_DRAW_REALIZE (VFW. h)
description: a \_ mensagem ICM DRAW \_ percebem notifica um driver de renderização para perceber sua paleta de desenho durante o desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- mensagem de ICM_DRAW_REALIZE Windows multimídia
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05e9bd21cc8185afd17ec909fcf95bf3ac6bedba7477f47191b9f3d51383914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987241"
---
# <a name="icm_draw_realize-message"></a>ICM \_ DESENHAR a \_ mensagem de percepção

a mensagem **ICM \_ DRAW \_ percebem** notifica um driver de renderização para perceber sua paleta de desenho durante o desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*HDC*
</dt> <dd>

Manipule o controlador de domínio usado para obter a paleta.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Sinalizador de plano de fundo. Especifique **true** para compreender a paleta como uma tarefa em segundo plano ou **false** para perceber a paleta em primeiro plano.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a paleta de desenho for realizada ou ICERR \_ sem suporte se a paleta associada aos dados descompactados for realizada.

## <a name="remarks"></a>Comentários

Os drivers só precisarão responder a esta mensagem se a paleta de desenho for diferente da paleta descompactada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





