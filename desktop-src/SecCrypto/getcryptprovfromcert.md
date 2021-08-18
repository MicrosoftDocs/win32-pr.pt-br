---
description: Obtém um handle para um CSP (provedor de serviços de criptografia) e uma especificação de chave para um contexto de certificado.
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
ms.openlocfilehash: c885c439014a26bafba3be8614981c67d200e9f87cd4e3c4f03e8cbcc1b77e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006654"
---
# <a name="getcryptprovfromcert-function"></a>Função GetCryptProvFromCert

> [!IMPORTANT]
> Essa API está preterida. A Microsoft pode remover essa API em versões futuras.

 

A **função GetCryptProvFromCert** obtém um handle para um CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) e uma especificação de chave para um [*contexto de*](../secgloss/c-gly.md) certificado. Use essa função para obter acesso à [*chave privada*](../secgloss/p-gly.md) do emissor do certificado.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

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

*hwnd* \[ Em\]
</dt> <dd>

O alça da janela a ser usada como o proprietário de todas as caixas de diálogo exibidas. Esse membro não é usado no momento e é ignorado. É seguro passar **NULL para** esse parâmetro.

</dd> <dt>

*pCert* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura DE \_ CONTEXTO DE**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) CERTIFICADO para o certificado.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Um ponteiro para uma [**estrutura HCRYPTPROV**](hcryptprov.md) que é um ponteiro para o CSP.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

A especificação da chave privada a ser recuperada. Os valores possíveis **\_ incluem AT KEYEXCHANGE** **ou AT \_ SIGNATURE.**

</dd> <dt>

*pfDidCryptAcquire* \[ Em\]
</dt> <dd>

Um valor que especifica se a função adquiriu o handle do provedor com base no certificado.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária. A **função GetCryptProvFromCert** fornece e inicializa o contêiner temporário. Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um **valor NULL.**

</dd> <dt>

*ppwszProviderName* \[ out, opcional\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do provedor. A **função GetCryptProvFromCert** retorna o nome do provedor. Ao chamar **GetCryptProvFromCert**, o endereço deve apontar para um **valor NULL.**

</dd> <dt>

*pdwProviderType* \[ out\]
</dt> <dd>

Especifica o tipo CSP. Pode ser zero ou um dos Tipos de Provedor [Criptográfico.](cryptographic-provider-types.md) Se esse membro for zero, o contêiner de chave será um dos provedores de armazenamento de chaves CNG.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Após o sucesso, essa função retorna **TRUE.** A **função GetCryptProvFromCert** retornará **FALSE** se falhar.

## <a name="remarks"></a>Comentários

A [ferramenta MakeCert](makecert.md) chama **GetCryptProvFromCert** quando você a invoca usando a opção de linha de comando **-is.**

Se o *parâmetro pfDidCryptAcquire* for definido como **TRUE,** a função definirá os parâmetros *phCryptProv*, *pdwKeySpec* e *pdwProviderType* para os valores do provedor.

Quando terminar de usar o CSP, livre-o chamando a [**função FreeCryptProvFromCert.**](freecryptprovfromcert.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
