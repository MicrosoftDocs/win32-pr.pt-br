---
title: Mensagem de ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: A \_ mensagem de paleta do conjunto de DEScompactação ICM \_ \_ especifica uma paleta para um driver de descompactação de vídeo a ser usado se estiver descompactando para um formato que usa uma paleta. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_SET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759629"
---
# <a name="icm_decompress_set_palette-message"></a>Mensagem de paleta do conjunto de \_ DEScompactação ICM \_ \_

A mensagem de **\_ paleta do \_ conjunto \_ de descompactação ICM** especifica uma paleta para um driver de descompactação de vídeo a ser usado se estiver descompactando para um formato que usa uma paleta. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) cuja tabela de cores contém as cores que devem ser usadas, se possível. Você pode especificar zero para usar o conjunto padrão de cores de saída.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se o driver de descompactação puder descompactar precisamente as imagens para a paleta sugerida usando o conjunto de cores conforme elas forem organizadas na paleta. Retorna ICERR \_ sem suporte.

## <a name="remarks"></a>Comentários

Esta mensagem não deve afetar a descompactação já em andamento; em vez disso, as cores passadas usando essa mensagem devem ser retornadas em resposta ao futuro [**ICM \_ descompactar \_ Get \_ Format**](icm-decompress-get-format.md) e [**ICM \_ descompactar \_ \_**](icm-decompress-get-palette.md) as mensagens da paleta. As cores são enviadas de volta para o driver de descompactação em uma futura mensagem de [**\_ \_ início de descompactação ICM**](icm-decompress-begin.md) .

Essa mensagem é usada principalmente quando um driver Descompacte imagens na tela e outro aplicativo que usa uma paleta está em primeiro plano, forçando o driver de descompactação a se adaptar a um conjunto de cores estrangeiro.

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

 

