---
description: A função DeleteExtractedFiles exclui os arquivos extraídos pela função Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Função DeleteExtractedFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753771"
---
# <a name="deleteextractedfiles-function"></a>Função DeleteExtractedFiles

\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]

A função **DeleteExtractedFiles** exclui os arquivos extraídos pela função [**Extract**](extract.md) .

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*profissionais* 
</dt> <dd>

Um ponteiro para uma estrutura de [**sessão**](session.md) que contém informações sobre a sessão atual.

Essa função libera a memória no membro **pFileList** dessa estrutura e define **pFileList** como **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Extração**](extract.md)
</dt> <dt>

[**SESSÃO**](session.md)
</dt> </dl>

 

 
