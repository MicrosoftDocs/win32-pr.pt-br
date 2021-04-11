---
title: Mensagem de WM_CAP_FILE_ALLOCATE (VFW. h)
description: A \_ mensagem de alocação de arquivo do WM Cap \_ \_ cria (prefixa) um arquivo de captura de um tamanho especificado. Você pode enviar essa mensagem explicitamente ou usando a macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- Multimídia do Windows de mensagem WM_CAP_FILE_ALLOCATE
topic_type:
- apiref
api_name:
- WM_CAP_FILE_ALLOCATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d36cec54e5775641118679b24b0d4b3b1767693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454859"
---
# <a name="wm_cap_file_allocate-message"></a>\_Mensagem de \_ alocação de arquivo do WM Cap \_

A mensagem de **\_ \_ \_ alocação de arquivo do WM Cap** cria (prefixa) um arquivo de captura de um tamanho especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) .


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*dwSize*
</dt> <dd>

Tamanho, em bytes, para criar o arquivo de captura.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Você pode melhorar significativamente o desempenho da captura de fluxo ao alocar um arquivo de captura grande o suficiente para armazenar um clipe de vídeo inteiro e desfragmentar o arquivo de captura antes de capturar o clipe.

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

 

 





