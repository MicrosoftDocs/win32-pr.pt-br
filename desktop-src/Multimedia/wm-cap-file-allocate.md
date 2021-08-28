---
title: WM_CAP_FILE_ALLOCATE mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ FILE \_ ALLOCATE cria (pré-aloca) um arquivo de captura de um tamanho especificado. Você pode enviar essa mensagem explicitamente ou usando a macro capFileAlloc.
ms.assetid: 31ebe824-4a30-4212-9479-a5cbd8fc1e1d
keywords:
- WM_CAP_FILE_ALLOCATE mensagem Windows Multimídia
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
ms.openlocfilehash: e76f0e88642d7d28771090b0690191eb4e4e72f5749dc74a9e42d90bfea87812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781396"
---
# <a name="wm_cap_file_allocate-message"></a>Mensagem WM \_ CAP \_ FILE \_ ALLOCATE

A **mensagem WM CAP FILE \_ \_ \_ ALLOCATE** cria (pré-aloca) um arquivo de captura de um tamanho especificado. Você pode enviar essa mensagem explicitamente ou usando a [**macro capFileAlloc.**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc)


```C++
WM_CAP_FILE_ALLOCATE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (DWORD) (dwSize); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>*Dwsize*
</dt> <dd>

Tamanho, em bytes, para criar o arquivo de captura.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Você pode melhorar significativamente o desempenho da captura de streaming, pré-localizando um arquivo de captura grande o suficiente para armazenar um clipe de vídeo inteiro e desfragmentando o arquivo de captura antes de capturar o clipe.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





