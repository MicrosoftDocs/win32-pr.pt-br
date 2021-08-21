---
title: WM_CAP_FILE_GET_CAPTURE_FILE mensagem (Vfw.h)
description: A mensagem WM \_ CAP FILE GET CAPTURE FILE retorna o nome do arquivo de captura \_ \_ \_ \_ atual. Você pode enviar essa mensagem explicitamente ou usando a macro capFileGetCaptureFile.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE mensagem Windows Multimídia
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
ms.openlocfilehash: 462f919458078129f6756782c2fde5322b3cd814c3108cb0ba8ee24e2f54c022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135314"
---
# <a name="wm_cap_file_get_capture_file-message"></a>Mensagem WM \_ CAP FILE GET CAPTURE \_ \_ \_ \_ FILE

A **mensagem WM CAP FILE GET CAPTURE \_ \_ \_ \_ \_ FILE** retorna o nome do arquivo de captura atual. Você pode enviar essa mensagem explicitamente ou usando a [**macro capFileGetCaptureFile.**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile)


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*Wsize*
</dt> <dd>

Tamanho, em bytes, do buffer definido pelo aplicativo referenciado **por szName.**

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*Szname*
</dt> <dd>

Ponteiro para um buffer definido pelo aplicativo usado para retornar o nome do arquivo de captura como uma cadeia de caracteres terminada em nulo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

O nome de arquivo de captura padrão é C: \\CAPTURE.AVI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





