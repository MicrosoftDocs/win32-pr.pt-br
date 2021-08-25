---
title: Mensagem de ICM_ABOUT (VFW. h)
description: a ICM \_ sobre a mensagem notifica um driver de compactação de vídeo para exibir sua caixa de diálogo about ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo about. Você pode enviar essa mensagem explicitamente ou usando a macro ICAbout.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- mensagem de ICM_ABOUT Windows multimídia
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf47ff93ef1986d805b2cb37697fdf4d86876c5552fe6aeffb00ff172673018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785066"
---
# <a name="icm_about-message"></a>ICM \_ SOBRE a mensagem

a **ICM \_ sobre** a mensagem notifica um driver de compactação de vídeo para exibir sua caixa de diálogo about ou consulta um driver de compactação de vídeo para determinar se ele tem uma caixa de diálogo about. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) .


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Identificador para a janela pai da caixa de diálogo exibida. Você também pode determinar se um driver tem uma caixa de diálogo about especificando-1 nesse parâmetro, como na macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) . O driver retornará ICERR \_ OK se ele tiver uma caixa de diálogo about ou ICERR \_ sem suporte, caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver der suporte a essa mensagem ou ICERR \_ sem suporte.

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

 

 





