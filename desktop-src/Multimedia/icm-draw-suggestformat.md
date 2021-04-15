---
title: Mensagem de ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: A \_ mensagem ICM Draw \_ SUGGESTFORMAT consulta um driver de renderização para sugerir um formato descompactado que pode ser desenhado.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_SUGGESTFORMAT
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454808"
---
# <a name="icm_draw_suggestformat-message"></a>\_Mensagem de desenho SUGGESTFORMAT de ICM \_

A mensagem **ICM \_ draw \_ SUGGESTFORMAT** consulta um driver de renderização para sugerir um formato descompactado que pode ser desenhado.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Ponteiro para uma estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se tiver êxito. Se o membro **lpbiSuggest** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) for **NULL**, essa mensagem retornará a quantidade de memória necessária para conter o formato sugerido.

## <a name="remarks"></a>Comentários

O driver deve examinar o formato especificado no membro **lpbiIn** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usar o membro **lpbiSuggest** para retornar um formato que ele possa desenhar. O formato de saída deve preservar o máximo de dados possível do formato de entrada.

Opcionalmente, o driver pode usar o identificador de compressor instalável passado no membro **hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) para fazer seleções mais complexas. Por exemplo, se o formato de entrada for de dados JPEG de 24 bits, um renderizador poderá consultar o descompactador para descobrir se ele pode ser descompactado para um formato YUV (que pode ser desenhado com mais eficiência) antes de selecionar o formato a ser sugerido.

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

 

 





