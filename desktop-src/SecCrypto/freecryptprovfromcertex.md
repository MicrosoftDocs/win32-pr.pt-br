---
description: 'Libera o identificador para um CSP (provedor de serviços de criptografia) ou para uma chave de Cryptography API: próxima geração (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Função FreeCryptProvFromCertEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829540"
---
# <a name="freecryptprovfromcertex-function"></a>Função FreeCryptProvFromCertEx

A função **FreeCryptProvFromCertEx** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) ou para uma chave de Cryptography API: próxima geração (CNG).

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
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

Um identificador para um CSP capicor ou um identificador para uma chave CNG.

</dd> <dt>

*dwKeySpec* 
</dt> <dd>

O endereço de uma variável **DWORD** que recebe informações adicionais sobre a chave. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                | Significado                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**em \_ troca de**</dt> </dl>                     | O par de chaves é um par de troca de chaves.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**NA \_ assinatura**</dt> </dl>                           | O par de chaves é um par de assinaturas.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**especificação de chave de certificado \_ NCRYPT \_ \_**</dt> </dl> | A chave é uma chave CNG.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |



 

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
