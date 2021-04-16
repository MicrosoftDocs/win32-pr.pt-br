---
title: Mensagem de ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: O ICM \_ DEScompactar a \_ \_ mensagem obter paleta solicita que o driver de descompactação de vídeo forneça a tabela de cores da estrutura BITMAPINFOHEADER de saída. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_GET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758608"
---
# <a name="icm_decompress_get_palette-message"></a>ICM- \_ compactar \_ \_ mensagem obter paleta

O **ICM \_ descompactar a mensagem \_ obter \_ paleta** solicita que o driver de descompactação de vídeo forneça a tabela de cores da estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de saída. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contém o formato de entrada.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) para conter a tabela de cores. O espaço reservado para a tabela de cores é sempre pelo menos 256 cores. Você pode especificar zero para esse parâmetro para retornar apenas o tamanho da tabela de cores.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se *lpbiOutput* for diferente de zero, o driver definirá o membro **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) como o número de cores na tabela de cores. O driver preenche o membro **bmiColors** de [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com as cores reais.

O driver deve dar suporte a essa mensagem somente se usar uma paleta diferente da especificada no formato de entrada.

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

 

