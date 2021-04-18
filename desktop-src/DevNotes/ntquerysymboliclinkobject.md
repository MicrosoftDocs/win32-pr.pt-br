---
description: Recupera o destino de um link simbólico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Função NtQuerySymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751952"
---
# <a name="ntquerysymboliclinkobject-function"></a>Função NtQuerySymbolicLinkObject

\[Essa função pode ser alterada ou não estar disponível no futuro.\]

Recupera o destino de um link simbólico.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LinkHandle* \[ no\]
</dt> <dd>

Um identificador para o objeto de vínculo simbólico.

</dd> <dt>

*LinkTarget* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode inicializada que recebe o destino do link simbólico. O **MaximumLength** e os membros do **buffer** devem ser definidos se a chamada falhar.

</dd> <dt>

*ReturnedLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o comprimento da cadeia de caracteres Unicode retornado no parâmetro *LinkTarget* . Se a função retornar **o \_ buffer de status \_ muito \_ pequeno**, essa variável receberá o tamanho de buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o **status \_ êxito** ou um status de erro.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
