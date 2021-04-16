---
description: Recupera o título do arquivo para o caminho de arquivo especificado.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: função pSetupGetFileTitle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751551"
---
# <a name="psetupgetfiletitle-function"></a>função pSetupGetFileTitle

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Recupera o título do arquivo para o caminho de arquivo especificado.

## <a name="syntax"></a>Sintaxe


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FilePath* \[ no\]
</dt> <dd>

O caminho do arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um ponteiro para cadeia de caracteres que recebe o título do arquivo.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
