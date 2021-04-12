---
title: Mensagem de ICM_COMPRESS_GET_FORMAT (VFW. h)
description: A \_ mensagem ICM Compact \_ Get \_ Format solicita o formato de saída dos dados compactados de um driver de compactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_GET_FORMAT
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455730"
---
# <a name="icm_compress_get_format-message"></a>\_Mensagem de \_ formato de obtenção do ICM Compact \_

A mensagem **ICM \_ Compact \_ Get \_ Format** solicita o formato de saída dos dados compactados de um driver de compactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .


```C++
ICM_COMPRESS_GET_FORMAT 
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

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para conter o formato de saída. Você pode especificar zero para esse parâmetro para solicitar apenas o tamanho do formato de saída, como na macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Se *lpbiOutput* for zero, retornará o tamanho da estrutura.

Se *lpbiOutput* for diferente de zero, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se *lpbiOutput* for diferente de zero, o driver deverá preencher a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com o formato de saída padrão correspondente ao formato de entrada especificado para *lpbiInput*. Se o compressor puder produzir vários formatos, o formato padrão deverá ser o que preserva a maior quantidade de informações.

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

 

