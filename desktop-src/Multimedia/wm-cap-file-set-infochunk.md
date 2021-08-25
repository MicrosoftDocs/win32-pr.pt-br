---
title: Mensagem de WM_CAP_FILE_SET_INFOCHUNK (VFW. h)
description: O arquivo do WM \_ Cap \_ \_ set \_ INFOCHUNK Message define e limpa as partes de informações.
ms.assetid: 67d11a05-a2b4-45d2-ba66-83a198745303
keywords:
- mensagem de WM_CAP_FILE_SET_INFOCHUNK Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_INFOCHUNK
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d64f88a87af63e5afc513e0e2cf2df53d64570bec099a2f8f2846d781fc0b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892066"
---
# <a name="wm_cap_file_set_infochunk-message"></a>\_Mensagem de \_ INFOCHUNK do conjunto de arquivos \_ \_ do WM Cap

O **arquivo do WM \_ Cap \_ \_ set \_ INFOCHUNK** Message define e limpa as partes de informações. As partes de informações podem ser inseridas em um arquivo AVI durante a captura para inserir cadeias de caracteres de texto ou dados personalizados. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .


```C++
WM_CAP_FILE_SET_INFOCHUNK 
wParam = (WPARAM)0; 
lParam = (LPARAM) (LPCAPINFOCHUNK) (lpInfoChunk); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpInfoChunk"></span><span id="lpinfochunk"></span><span id="LPINFOCHUNK"></span>*lpInfoChunk*
</dt> <dd>

Ponteiro para uma estrutura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) que define a parte das informações a ser criada ou excluída.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Várias partes de informações registradas podem ser adicionadas a um arquivo AVI. Depois que uma parte de informações é definida, ela continua a ser adicionada aos arquivos de captura subsequentes até que a entrada seja desmarcada ou todas as entradas de partes de informações sejam limpas. Para limpar uma única entrada, especifique a parte das informações no membro **fccInfoID** e **NULL** no membro **lpData** da estrutura [**CAPINFOCHUNK**](/windows/win32/api/vfw/ns-vfw-capinfochunk) . Para limpar todas as entradas, especifique **NULL** em **fccInfoID**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





