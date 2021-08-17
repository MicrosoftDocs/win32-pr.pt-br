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
ms.openlocfilehash: 805f3de5da380c4749e58dd7467f1f4ccb2471119ffed81b79695a98feb1b090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003626"
---
# <a name="ntquerysymboliclinkobject-function"></a>Função NtQuerySymbolicLinkObject

\[Essa função pode ser alterada ou não disponível no futuro.\]

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

*LinkHandle* \[ Em\]
</dt> <dd>

Um identificador para o objeto de link simbólico.

</dd> <dt>

*LinkTarget* \[ in, out\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode inicializada que recebe o destino do link simbólico. Os **membros MaximumLength** **e Buffer** deverão ser definidos se a chamada falhar.

</dd> <dt>

*ReturnedLength* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável que recebe o comprimento da cadeia de caracteres Unicode retornada no *parâmetro LinkTarget.* Se a função retornar **STATUS \_ BUFFER MUITO \_ \_ PEQUENO**, essa variável receberá o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna **STATUS \_ SUCCESS ou** um status de erro.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NtOpenSymbolicLinkObject**](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
