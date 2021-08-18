---
description: 'Libera o handle para um CSP (provedor de serviços de criptografia) ou para uma chave CNG (Cryptography API: Next Generation).'
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
ms.openlocfilehash: b887fd7cd37e8963430378590552273b0856dc2cf73e9d0da15ab41a5a622447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006734"
---
# <a name="freecryptprovfromcertex-function"></a>Função FreeCryptProvFromCertEx

A **função FreeCryptProvFromCertEx** libera [*o*](../secgloss/c-gly.md) handle para um CSP (provedor de serviços de criptografia) ou para uma chave CNG (Api de Criptografia: Próxima Geração).

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

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

*fAcquired* \[ Em\]
</dt> <dd>

Um valor que especifica se o handle do provedor foi adquirido do [*certificado*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ Em\]
</dt> <dd>

Um alça para um CSP CAPICOM ou um alça para uma chave CNG.

</dd> <dt>

*Dwkeyspec* 
</dt> <dd>

O endereço de uma **variável DWORD** que recebe informações adicionais sobre a chave. Esse pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                | Significado                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> </dl>                     | O par de chaves é um par de troca de chaves.<br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ SIGNATURE**</dt> </dl>                           | O par de chaves é um par de assinaturas.<br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <dt>**CERT \_ NCRYPT \_ KEY \_ SPEC**</dt> </dl> | A chave é uma chave CNG.<br/> **Windows Server 2003 e Windows XP:** Não há suporte para esse valor.<br/> |



 

</dd> <dt>

*pwszCapiProvider* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor.

</dd> <dt>

*dwProviderType* \[ Em\]
</dt> <dd>

Especifica o tipo CSP. Pode ser zero ou um dos Tipos de Provedor [Criptográfico.](cryptographic-provider-types.md) Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.

</dd> <dt>

*pwszTmpContainer* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
