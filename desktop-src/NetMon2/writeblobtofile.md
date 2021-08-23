---
description: A função WriteBlobToFile grava um BLOB em um arquivo.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Função WriteBlobToFile (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 045762837727308beb9b80a5854258b04cb02c0886cce9c2318032f5395b57fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742176"
---
# <a name="writeblobtofile-function"></a>Função WriteBlobToFile

A **função WriteBlobToFile** grava um BLOB em um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB.

</dd> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Ponteiro para o nome do arquivo, no qual o BLOB é salvo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




