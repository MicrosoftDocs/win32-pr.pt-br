---
title: Mensagem de WM_CAP_GET_MCI_DEVICE (VFW. h)
description: A mensagem do dispositivo do WM \_ Cap \_ Get \_ MCI \_ recupera o nome de um dispositivo MCI definido anteriormente com \_ a \_ \_ mensagem do dispositivo MCI de conjunto de Cap do WM \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capGetMCIDeviceName.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_MCI_DEVICE
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
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454598"
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

 

 





