---
title: Mensagem de WM_CAP_SET_MCI_DEVICE (VFW. h)
description: A \_ mensagem do dispositivo MCI do conjunto de Cap do WM \_ \_ \_ especifica o nome do dispositivo de vídeo MCI a ser usado para capturar dados. Você pode enviar essa mensagem explicitamente ou usando a macro capSetMCIDeviceName.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_MCI_DEVICE
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644288"
---
# <a name="wm_cap_set_mci_device-message"></a>\_Mensagem do \_ \_ dispositivo MCI do conjunto de Cap do WM \_

A mensagem do **\_ \_ \_ \_ dispositivo MCI do conjunto de Cap do WM** especifica o nome do dispositivo de vídeo MCI a ser usado para capturar dados. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) .


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem armazena o nome do dispositivo MCI em uma estrutura interna. Ele não abre nem acessa o dispositivo. O nome do dispositivo padrão é **NULL**.

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

 

 





