---
title: ICM_DECOMPRESS_BEGIN mensagem (Vfw.h)
description: A ICM DECOMPRESS BEGIN notifica um driver de descompactação de vídeo para se preparar \_ \_ para descompactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN mensagem Windows Multimídia
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
ms.openlocfilehash: f1d26a0ea99f089d558da639dfad99d4551237b180e595912973e0d22f634f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678346"
---
# <a name="icm_decompress_begin-message"></a>\_ICM Mensagem DECOMPRESS \_ BEGIN

A **ICM \_ DECOMPRESS \_ BEGIN** notifica um driver de descompactação de vídeo para se preparar para descompactar dados. Você pode enviar essa mensagem explicitamente ou usando a [**macro ICDecompressBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin)


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma [**estrutura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Ponteiro para uma [**estrutura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a descompactação especificada tiver suporte ou ICERR \_ BADFORMAT caso contrário.

## <a name="remarks"></a>Comentários

Quando o driver recebe essa mensagem, ele deve alocar buffers e fazer operações demoradas para que ele possa processar ICM [**\_ mensagens DECOMPRESS**](icm-decompress.md) com eficiência.

Se você quiser que o driver descompacte os dados diretamente para a tela, envie a [**mensagem \_ ICM DRAW.**](icm-draw.md)

As **ICM \_ DECOMPRESS \_ BEGIN** e [**as ICM \_ DECOMPRESS \_ END**](icm-decompress-end.md) não são aninhadas. Se o driver receber **ICM \_ DECOMPRESS \_ BEGIN** antes que a descompactação seja interrompida com **ICM \_ DECOMPRESS \_ END**, ele deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

