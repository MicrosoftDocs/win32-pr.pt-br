---
title: Mensagem de WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: A \_ mensagem de configuração de sequência Get da Cap do WM \_ \_ \_ recupera as configurações atuais dos parâmetros de captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- mensagem de WM_CAP_GET_SEQUENCE_SETUP Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55122a98846f23c609eb371ab5698198729c39e967d7953295850b61764459af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369534"
---
# <a name="wm_cap_get_sequence_setup-message"></a>\_Mensagem de \_ \_ configuração da sequência get \_ do WM Cap

A mensagem de **\_ \_ \_ \_ configuração de sequência Get da Cap do WM** recupera as configurações atuais dos parâmetros de captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*&*
</dt> <dd>

Ponteiro para uma estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Para obter informações sobre os parâmetros usados para controlar a captura de streaming, consulte a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

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

 

 





