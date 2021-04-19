---
description: Recupera os atributos básicos para o objeto de arquivo especificado.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Função NtQueryAttributesFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756512"
---
# <a name="ntqueryattributesfile-function"></a>Função NtQueryAttributesFile

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Recupera os atributos básicos para o objeto de arquivo especificado.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Objetoattributes* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) que fornece os atributos a serem usados para o objeto de arquivo.

</dd> <dt>

*Informações* \[ do fora\]
</dt> <dd>

Um ponteiro para uma estrutura de [ \_ \_ informações básicas de arquivo](https://msdn.microsoft.com/library/aa491634.aspx) para receber as informações de atributo de arquivo retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um NTSTATUS ou um código de erro.

Os formulários e o significado dos códigos de erro NTSTATUS são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no WDK. Você também pode usar as funções [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




