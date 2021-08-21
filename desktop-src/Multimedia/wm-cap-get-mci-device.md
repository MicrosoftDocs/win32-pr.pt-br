---
title: Mensagem de WM_CAP_GET_MCI_DEVICE (VFW. h)
description: A mensagem do dispositivo do WM \_ Cap \_ Get \_ MCI \_ recupera o nome de um dispositivo MCI definido anteriormente com \_ a \_ \_ mensagem do dispositivo MCI de conjunto de Cap do WM \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- mensagem de WM_CAP_GET_MCI_DEVICE Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9471177693bfbd5646d93e8487395cdf330b8281a1f43fa00d79dc690e6d718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800646"
---
# <a name="wm_cap_get_mci_device-message"></a>\_Mensagem do \_ \_ dispositivo MCI da obtenção do WM Cap \_

A mensagem do **dispositivo do WM \_ Cap \_ Get \_ MCI \_** recupera o nome de um dispositivo MCI definido anteriormente com a mensagem do [**\_ \_ \_ \_ dispositivo MCI de conjunto de Cap do WM**](wm-cap-set-mci-device.md) . Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) .


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Comprimento, em bytes, do buffer referenciado por **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo MCI.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

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

 

 





