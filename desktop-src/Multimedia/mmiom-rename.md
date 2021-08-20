---
title: MMIOM_RENAME mensagem (Mmsystem.h)
description: A mensagem MMIOM RENAME é enviada a um procedimento de E/S pela função mmioRename para solicitar que o arquivo especificado \_ seja renomeado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065306"
---
# <a name="mmiom_rename-message"></a>Mensagem MMIOM \_ RENAME

A **mensagem MMIOM \_ RENAME** é enviada a um procedimento de E/S pela [**função mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) para solicitar que o arquivo especificado seja renomeado.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do arquivo a ser renomedo.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o novo nome de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Se o arquivo for renomeado com êxito, o valor de retorno será zero. Se o arquivo especificado não for encontrado, o valor de retorno será MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

