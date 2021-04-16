---
title: Mensagem de WM_CAP_DRIVER_GET_NAME (VFW. h)
description: A \_ \_ \_ mensagem obter nome do driver do WM Cap \_ retorna o nome do driver de captura conectado à janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_GET_NAME
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454860"
---
# <a name="wm_cap_driver_get_name-message"></a>\_Mensagem de \_ \_ nome Get do driver do WM Cap \_

A **mensagem \_ \_ \_ obter \_ nome do driver do WM Cap** retorna o nome do driver de captura conectado à janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, do buffer referenciado por **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar o nome do dispositivo como uma cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

O nome é uma cadeia de caracteres de texto recuperada da área de recursos do driver. Os aplicativos devem alocar aproximadamente 80 bytes para essa cadeia de caracteres. Se o driver não contiver um recurso de nome, o nome de caminho completo do driver listado no registro ou no arquivo de SYSTEM.INI será retornado.

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

 

 





