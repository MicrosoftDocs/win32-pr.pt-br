---
title: Mensagem de ICM_DECOMPRESS_BEGIN (VFW. h)
description: A mensagem de início do ICM \_ DEScompactar \_ Notifica um driver de descompactação de vídeo para se preparar para descompactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_BEGIN
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086141"
---
# <a name="icm_decompress_begin-message"></a>Mensagem de início do ICM \_ DEScompactar \_

A mensagem de **início do ICM \_ descompactar \_** notifica um driver de descompactação de vídeo para se preparar para descompactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.

## <a name="remarks"></a>Comentários

Quando o driver recebe essa mensagem, ele deve alocar buffers e realizar operações demoradas para que possa processar com eficiência as mensagens do [**ICM \_**](icm-decompress.md) .

Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .

As mensagens de [**\_ \_ término**](icm-decompress-end.md) do **ICM \_ Descompacte \_ begin** e ICM não são aninhadas. Se o driver receber **a \_ descompactação ICM \_ começar** antes que a descompactação seja interrompida com o **\_ \_ ponto de descompactação ICM**, ela deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

