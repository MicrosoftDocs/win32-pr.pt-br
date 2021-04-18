---
description: Abre um identificador para um objeto de thread com o acesso especificado.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Função NtOpenThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751752"
---
# <a name="ntopenthread-function"></a>Função NtOpenThread

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio. Em vez disso, use a função [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]

Abre um identificador para um objeto de thread com o acesso especificado.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ThreadHandle* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o identificador de objeto de thread.

</dd> <dt>

*DesiredAccess* \[ no\]
</dt> <dd>

Um tipo de dados de [**\_ máscara de acesso**](../secauthz/access-mask-format.md) que fornece os tipos de acesso desejados para o objeto de thread.

</dd> <dt>

*Objetoattributes* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) . O membro **objectname** desta estrutura deve ser nulo.

**Windows Server 2003 e Windows XP:** O membro **objectname** desta estrutura pode apontar para um nome de objeto. Se **objectname** não for NULL, o parâmetro *CLIENTID* deverá ser nulo.

</dd> <dt>

*ClientID* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de **\_ ID do cliente** que identifica o thread cujo thread deve ser aberto.

**Windows Server 2003 e Windows XP:** Um ponteiro para uma estrutura de **\_ ID do cliente** que identifica o thread cujo thread deve ser aberto. Este parâmetro pode ser NULL. Se esse parâmetro não for nulo, o membro **objectname** da estrutura apontada pelo parâmetro *objectAttributes* deverá ser nulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **NTSTATUS** ou um código de erro.

Os formulários e o significado dos códigos de erro **NTSTATUS** são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no WDK. Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
