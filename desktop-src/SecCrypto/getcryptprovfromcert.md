---
description: Obtém um identificador para um CSP (provedor de serviços de criptografia) e uma especificação de chave para um contexto de certificado.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Função GetCryptProvFromCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297674"
---
# <a name="getcryptprovfromcert-function"></a>Função GetCryptProvFromCert

> [!IMPORTANT]
> Essa API está preterida. A Microsoft poderá remover essa API em versões futuras.

 

A função **GetCryptProvFromCert** Obtém um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e uma especificação de chave para um contexto de [*certificado*](../secgloss/c-gly.md) . Use essa função para obter acesso à [*chave privada*](../secgloss/p-gly.md) do emissor do certificado.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

O identificador da janela a ser usada como o proprietário de qualquer caixa de diálogo exibida. Esse membro não é usado no momento e é ignorado. É seguro passar **NULL** para esse parâmetro.

</dd> <dt>

*pCert* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para o certificado.

</dd> <dt>

*phCryptProv* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**HCRYPTPROV**](hcryptprov.md) que é um identificador para o CSP.

</dd> <dt>

*pdwKeySpec* \[ fora\]
</dt> <dd>

A especificação da chave privada a ser recuperada. Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.

</dd> <dt>

*pfDidCryptAcquire* \[ no\]
</dt> <dd>

Um valor que especifica se a função adquiriu o identificador do provedor com base no certificado.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária. A função **GetCryptProvFromCert** fornece e inicializa o contêiner temporário. Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um valor **nulo** .

</dd> <dt>

*ppwszProviderName* \[ out, opcional\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor. A função **GetCryptProvFromCert** retorna o nome do provedor. Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um valor **nulo** .

</dd> <dt>

*pdwProviderType* \[ fora\]
</dt> <dd>

Especifica o tipo de CSP. Isso pode ser zero ou um dos [tipos de provedor criptográfico](cryptographic-provider-types.md). Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Após o êxito, essa função retornará **true**. A função **GetCryptProvFromCert** retornará **false** se falhar.

## <a name="remarks"></a>Comentários

A ferramenta [MakeCert](makecert.md) chama **GetCryptProvFromCert** quando você a invoca usando a opção de linha de comando **-is** .

Se o parâmetro *pfDidCryptAcquire* for definido como **true**, a função definirá os parâmetros *phCryptProv*, *pdwKeySpec* e *pdwProviderType* para os valores do provedor.

Quando você terminar de usar o CSP, libere-o chamando a função [**FreeCryptProvFromCert**](freecryptprovfromcert.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
