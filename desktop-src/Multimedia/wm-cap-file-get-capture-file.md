---
title: Mensagem de WM_CAP_FILE_GET_CAPTURE_FILE (VFW. h)
description: A mensagem do arquivo de captura do arquivo do WM \_ Cap \_ \_ \_ \_ retorna o nome do arquivo de captura atual. Você pode enviar essa mensagem explicitamente ou usando a macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_GET_CAPTURE_FILE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824215"
---
# <a name="wm_cap_file_get_capture_file-message"></a>\_Mensagem do \_ \_ arquivo de obtenção de \_ captura de arquivo \_ do WM Cap

A mensagem do arquivo de **\_ \_ \_ \_ captura \_** do arquivo do WM Cap retorna o nome do arquivo de captura atual. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) .


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, do buffer definido pelo aplicativo referenciado por **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar o nome do arquivo de captura como uma cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O nome de arquivo de captura padrão é C: \\CAPTURE.AVI.

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

 

 





