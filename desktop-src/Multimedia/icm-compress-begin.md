---
title: Mensagem de ICM_COMPRESS_BEGIN (VFW. h)
description: A \_ mensagem de início de compactação ICM \_ Notifica um driver de compactação de vídeo para se preparar para compactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_BEGIN
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009748"
---
# <a name="icm_compress_begin-message"></a>\_Mensagem de início de compactação ICM \_

A mensagem de **\_ \_ início de compactação ICM** notifica um driver de compactação de vídeo para se preparar para compactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


```C++
ICM_COMPRESS_BEGIN 
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

Retornará ICERR \_ OK se o driver der suporte à compactação especificada ou ICERR \_ BADFORMAT se não houver suporte para o formato de entrada ou saída.

## <a name="remarks"></a>Comentários

O driver deve alocar e inicializar qualquer tabela ou memória necessária para compactar os formatos de dados quando ele recebe a mensagem [**ICM \_ compress**](icm-compress.md) .

VCM salva as configurações da mensagem de **\_ \_ início de compactação ICM** mais recente. As mensagens de término do **ICM \_ compacte \_ begin** e [**ICM \_ compress \_**](icm-compress-end.md) não são aninhadas. Se o driver receber **a \_ compactação de ICM, \_ comece** antes que a compactação seja interrompida com a **\_ \_ extremidade de compactação ICM**, ela deverá reiniciar a compactação com novos parâmetros

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

 

