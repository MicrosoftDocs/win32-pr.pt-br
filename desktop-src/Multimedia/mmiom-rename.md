---
title: Mensagem de MMIOM_RENAME (mmsystem. h)
description: A \_ mensagem de renomeação MMIOM é enviada a um procedimento de e/s pela função mmioRename para solicitar que o arquivo especificado seja renomeado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- Multimídia do Windows de mensagem MMIOM_RENAME
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
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455726"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ renomear mensagem

A mensagem de **\_ renomeação MMIOM** é enviada a um procedimento de e/s pela função [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) para solicitar que o arquivo especificado seja renomeado.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do arquivo a ser renomeado.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o novo nome de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Se o arquivo for renomeado com êxito, o valor de retorno será zero. Se o arquivo especificado não foi encontrado, o valor de retorno será MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

