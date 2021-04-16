---
description: A função ReadBlobFromFile lê um BLOB em um arquivo.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Função ReadBlobFromFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759481"
---
# <a name="readblobfromfile-function"></a>Função ReadBlobFromFile

A função **ReadBlobFromFile** lê um blob em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB.

</dd> <dt>

*pFileName* \[ no\]
</dt> <dd>

Ponteiro para o nome do arquivo que contém o BLOB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




