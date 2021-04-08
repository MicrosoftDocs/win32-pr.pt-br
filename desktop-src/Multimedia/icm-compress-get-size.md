---
title: Mensagem de ICM_COMPRESS_GET_SIZE (VFW. h)
description: A \_ mensagem ICM Compact \_ Get de \_ tamanho solicita que o driver de compactação de vídeo forneça o tamanho máximo de um quadro de dados quando compactados no formato de saída especificado. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_GET_SIZE
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918955"
---
# <a name="icm_compress_get_size-message"></a>ICM \_ compactar \_ mensagem de obtenção de \_ tamanho

A mensagem **ICM \_ Compact Get de \_ \_ tamanho** solicita que o driver de compactação de vídeo forneça o tamanho máximo de um quadro de dados quando compactados no formato de saída especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .


```C++
ICM_COMPRESS_GET_SIZE 
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

Retorna o número máximo de bytes que um único quadro compactado pode ocupar.

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos enviam essa mensagem para determinar o tamanho de um buffer a ser alocado para o quadro compactado.

O driver deve calcular o tamanho do maior quadro possível com base nos formatos de entrada e saída.

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

 

