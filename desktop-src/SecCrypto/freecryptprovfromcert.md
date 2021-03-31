---
description: Libera o identificador para um CSP (provedor de serviços de criptografia) e, opcionalmente, exclui o contêiner temporário criado pela função GetCryptProvFromCert.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Função FreeCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829541"
---
# <a name="freecryptprovfromcert-function"></a>Função FreeCryptProvFromCert

> [!IMPORTANT]
> Essa API está preterida. A Microsoft poderá remover essa API em versões futuras.

 

A função **FreeCryptProvFromCert** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e, opcionalmente, exclui o contêiner temporário criado pela função [**GetCryptProvFromCert**](getcryptprovfromcert.md) .

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fAcquired* \[ no\]
</dt> <dd>

Um valor que especifica se o identificador do provedor foi adquirido do [*certificado*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**HCRYPTPROV**](hcryptprov.md) para o CSP.

</dd> <dt>

*pwszCapiProvider* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor.

</dd> <dt>

*dwProviderType* \[ no\]
</dt> <dd>

Especifica o tipo de CSP. Isso pode ser zero ou um dos [tipos de provedor criptográfico](cryptographic-provider-types.md). Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.

</dd> <dt>

*pwszTmpContainer* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
