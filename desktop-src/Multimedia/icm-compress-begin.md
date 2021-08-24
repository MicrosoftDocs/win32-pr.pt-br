---
title: Mensagem de ICM_COMPRESS_BEGIN (VFW. h)
description: o ICM \_ compactar \_ mensagem de início notifica um driver de compactação de vídeo para se preparar para compactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- mensagem de ICM_COMPRESS_BEGIN Windows multimídia
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
ms.openlocfilehash: 33a6ee9c080e2dfc7a779abd4ae2a788bbe136ddcab1ef529714639065553ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140944"
---
# <a name="icm_compress_begin-message"></a>ICM \_ COMPACTar \_ mensagem de início

o **ICM \_ compactar \_** mensagem de início notifica um driver de compactação de vídeo para se preparar para compactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


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

o driver deve alocar e inicializar qualquer tabela ou memória necessária para compactar os formatos de dados quando ele recebe a mensagem [**ICM \_ comprimir**](icm-compress.md) .

VCM salva as configurações da mensagem de **\_ \_ início ICM compactar** mais recente. o **ICM \_ compactar \_ início** e ICM mensagens de [**\_ \_ término de compactação**](icm-compress-end.md) não são aninhadas. se o seu driver receber **ICM \_ compactar \_ começar** antes que a compactação seja interrompida com **ICM \_ \_ extremidade de compactação**, ela deverá reiniciar a compactação com novos parâmetros.

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

 

