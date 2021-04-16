---
description: Recupera informações sobre o objeto de diretório especificado.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Função NtQueryDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750132"
---
# <a name="ntquerydirectoryobject-function"></a>Função NtQueryDirectoryObject

\[Essa função pode ser alterada ou não estar disponível no futuro.\]

Recupera informações sobre o objeto de diretório especificado.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DirectoryHandle* \[ no\]
</dt> <dd>

Um identificador para o objeto de diretório.

</dd> <dt>

*Buffer* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer que recebe as informações do diretório. Esse buffer recebe uma ou mais estruturas de **\_ \_ informações de diretório de objeto** , a última sendo **NULL**, seguida por cadeias de caracteres que contêm os nomes das entradas de diretório. Para obter mais informações, consulte Comentários.

</dd> <dt>

*Comprimento* \[ no\]
</dt> <dd>

O tamanho do buffer de saída fornecido pelo usuário, em bytes.

</dd> <dt>

*ReturnSingleEntry* \[ no\]
</dt> <dd>

Indica se a função deve retornar apenas uma única entrada.

</dd> <dt>

*RestartScan* \[ no\]
</dt> <dd>

Indica se é para reiniciar a verificação ou continuar a enumeração usando as informações passadas no parâmetro de *contexto* .

</dd> <dt>

*Contexto* \[ do entrada, saída\]
</dt> <dd>

O contexto de enumeração.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o comprimento das informações de diretório retornadas no buffer de saída, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o **status \_ êxito** ou um status de erro.

## <a name="remarks"></a>Comentários

A seguir está a definição da estrutura **de \_ \_ informações do diretório de objeto** .

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NtOpenDirectoryObject**](ntopendirectoryobject.md)
</dt> </dl>

 

 
