---
title: Mensagem de ICM_DRAW_REALIZE (VFW. h)
description: A mensagem de desenho do ICM \_ draw \_ Notifica um driver de renderização para perceber sua paleta de desenho durante o desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_REALIZE
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
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369530"
---
# <a name="icm_draw_realize-message"></a>Mensagem de percepção de \_ desenho de ICM \_

A mensagem de **desenho do ICM \_ draw \_** notifica um driver de renderização para perceber sua paleta de desenho durante o desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


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

 

 





