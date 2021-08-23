---
title: ICM_DRAW_SUGGESTFORMAT mensagem (Vfw.h)
description: A ICM DRAW SUGGESTFORMAT consulta um driver de renderização para sugerir um formato \_ \_ descompactado que ele pode desenhar.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT mensagem Windows Multimídia
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
ms.openlocfilehash: 843dd2d398f5be6476a148922f3244113e94ab3fe3c10bac9ee08caefb8c4828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495945"
---
# <a name="icm_draw_suggestformat-message"></a>\_ICM Mensagem DRAW \_ SUGGESTFORMAT

A **ICM \_ DRAW \_ SUGGESTFORMAT** consulta um driver de renderização para sugerir um formato descompactado que ele pode desenhar.


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*
</dt> <dd>

Ponteiro para uma [**estrutura ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Tamanho, em bytes, [**de ICDRAWSUGGEST.**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido. Se o **membro lpbiSuggest** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) for **NULL,** essa mensagem retornará a quantidade de memória necessária para conter o formato sugerido.

## <a name="remarks"></a>Comentários

O driver deve examinar o formato especificado no membro **lpbiIn** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usar o membro **lpbiSuggest** para retornar um formato que ele pode desenhar. O formato de saída deve preservar o máximo de dados possível do formato de entrada.

Opcionalmente, o driver pode usar a alça de ltda instanciável passada no **membro hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) para fazer seleções mais complexas. Por exemplo, se o formato de entrada for dados JPEG de 24 bits, um renderador poderá consultar o descompactador para descobrir se ele pode ser descompactado em um formato YUV (que pode ser desenhado com mais eficiência) antes de selecionar o formato a sugerir.

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

 

 





