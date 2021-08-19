---
title: Mensagem de WM_CAP_DRIVER_GET_CAPS (VFW. h)
description: A \_ \_ mensagem obter Caps do driver do WM Cap \_ \_ retorna os recursos de hardware do driver de captura atualmente conectados a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetCaps.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- mensagem de WM_CAP_DRIVER_GET_CAPS Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aecc863234cddf64bece47896015fd01e97093d227951aef69363136e55cabe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687076"
---
# <a name="wm_cap_driver_get_caps-message"></a>\_Mensagem de \_ obtenção do driver \_ \_ do WM Cap

A **mensagem \_ \_ \_ obter \_ Caps do driver do WM Cap** retorna os recursos de hardware do driver de captura atualmente conectados a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) .


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*
</dt> <dd>

Ponteiro para a estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) para conter os recursos de hardware.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

Os recursos retornados em [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) são constantes para um determinado driver de captura. Os aplicativos precisam recuperar essas informações uma vez quando o driver de captura é conectado primeiro a uma janela de captura.

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

 

 





