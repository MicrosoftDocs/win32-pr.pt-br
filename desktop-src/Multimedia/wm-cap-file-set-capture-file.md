---
title: Mensagem de WM_CAP_FILE_SET_CAPTURE_FILE (VFW. h)
description: A mensagem do arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_ nomeia o arquivo usado para captura de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro capFileSetCaptureFile.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_SET_CAPTURE_FILE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917967"
---
# <a name="wm_cap_file_set_capture_file-message"></a>\_Mensagem do \_ \_ arquivo de captura do conjunto de arquivos do \_ WM Cap \_

A mensagem do **arquivo de captura do conjunto de arquivos do WM \_ Cap \_ \_ \_ \_** nomeia o arquivo usado para captura de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) .


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Ponteiro para a cadeia de caracteres terminada em nulo que contém o nome do arquivo de captura a ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se o nome de arquivo for inválido ou se a captura de streaming ou de quadro único estiver em andamento.

## <a name="remarks"></a>Comentários

Essa mensagem armazena o nome de arquivo em uma estrutura interna. Ele não cria, aloca ou abre o arquivo especificado. O nome de arquivo de captura padrão é C: \\CAPTURE.AVI.

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

 

 





