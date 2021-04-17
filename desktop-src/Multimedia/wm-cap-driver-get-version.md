---
title: Mensagem de WM_CAP_DRIVER_GET_VERSION (VFW. h)
description: A \_ \_ mensagem obter versão do driver do WM Cap \_ \_ retorna as informações de versão do driver de captura conectado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverGetVersion.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_GET_VERSION
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755072"
---
# <a name="wm_cap_driver_get_version-message"></a>\_Mensagem de \_ obtenção \_ de \_ versão do driver do WM Cap

A **mensagem \_ \_ \_ obter \_ versão do driver do WM Cap** retorna as informações de versão do driver de captura conectado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) .


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, do buffer definido pelo aplicativo referenciado por **szVer**.

</dd> <dt>

<span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar as informações de versão como uma cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

## <a name="remarks"></a>Comentários

As informações de versão são uma cadeia de texto recuperada da área de recursos do driver. Os aplicativos devem alocar aproximadamente 40 bytes para essa cadeia de caracteres. Se as informações de versão não estiverem disponíveis, uma cadeia de caracteres **nula** será retornada.

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

 

 





