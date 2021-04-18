---
title: Mensagem de ICM_COMPRESS_QUERY (VFW. h)
description: A \_ mensagem de consulta de compactação ICM \_ consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode compactar um formato de entrada específico para um formato de saída específico.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_QUERY
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768710"
---
# <a name="icm_compress_query-message"></a>\_Mensagem de consulta de compactação ICM \_

A mensagem de **\_ \_ consulta de compactação ICM** consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode compactar um formato de entrada específico para um formato de saída específico. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .


```C++
ICM_COMPRESS_QUERY 
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

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída. Você pode especificar zero para esse parâmetro para indicar que qualquer formato de saída é aceitável.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se a compactação especificada for suportada ou ICERR \_ BADFORMAT caso contrário.

## <a name="remarks"></a>Comentários

Quando um driver recebe essa mensagem, ele deve examinar a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) associada ao *lpbiInput* para determinar se ele pode compactar o formato de entrada.

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

 

