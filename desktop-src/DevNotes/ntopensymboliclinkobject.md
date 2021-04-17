---
description: Abre um link simbólico existente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Função NtOpenSymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811246"
---
# <a name="ntopensymboliclinkobject-function"></a>Função NtOpenSymbolicLinkObject

\[Essa função pode ser alterada ou não estar disponível no futuro.\]

Abre um link simbólico existente.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LinkHandle* \[ fora\]
</dt> <dd>

Um identificador para o objeto de link simbólico aberto recentemente.

</dd> <dt>

*DesiredAccess* \[ no\]
</dt> <dd>

Uma [**\_ máscara de acesso**](../secauthz/access-mask.md) que especifica o acesso solicitado ao objeto de diretório. É comum usar a leitura genérica para \_ que o identificador possa ser passado para a função [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .

</dd> <dt>

*Objetoattributes* \[ no\]
</dt> <dd>

Os atributos para o objeto de diretório. Para inicializar a estrutura de **\_ atributos de objeto** , use a macro **InitializeObjectAttributes** . Se o chamador não estiver em execução em um contexto de thread do sistema, ele deverá especificar o sinalizador **obj \_ kernel \_ Handle** ao inicializar a estrutura. Para obter mais informações, consulte a documentação para esses itens na documentação do WDK.

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

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
