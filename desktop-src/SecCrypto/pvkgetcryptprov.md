---
description: Obtém um handle para um CSP (provedor de serviços de criptografia) com base em um arquivo de chave privada ou em um nome de contêiner de chave.
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: Função PvkGetCryptProv
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 5ba60ca31bf75e355126484608bfe9650b00fea60eaf876022e2de2bf5030470
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901316"
---
# <a name="pvkgetcryptprov-function"></a>Função PvkGetCryptProv

> [!IMPORTANT]
> Essa API está preterida. A Microsoft pode remover essa API em versões futuras.

 

A **função PvkGetCryptProv** obtém um handle para um CSP [](../secgloss/p-gly.md) [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) com base em um arquivo de chave privada ou em um nome de contêiner de chave.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente ao Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwnd* \[ Em\]
</dt> <dd>

Se uma senha for necessária para descriptografar o arquivo de chave privada, esse parâmetro será um handle para o pai da caixa de diálogo de senha; caso contrário, será **NULL.**

</dd> <dt>

*pwszCaption* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para a legenda da caixa de diálogo.

</dd> <dt>

*pwszCapiProvider* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do CSP.

</dd> <dt>

*dwProviderType* \[ Em\]
</dt> <dd>

Um **valor DWORD** que representa o tipo de provedor criptográfico. Para obter mais informações, consulte [Cryptographic Provider Types](cryptographic-provider-types.md).

</dd> <dt>

*pwszPvkFile* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome de um arquivo de chave privada.

</dd> <dt>

*pwszKeyContainerName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave privada.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Um ponteiro para um **valor DWORD** para o tipo de chave do contêiner retornado com *phCryptProv* e *ppwszTmpContainer*.

</dd> <dt>

*ppwszTmpContainer* \[ out, opcional\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do contêiner de chave temporária. A **função PvkGetCryptProv** fornece e inicializa o contêiner temporário. Ao chamar **PvkGetCryptProv,** o endereço deve apontar para um **valor NULL.**

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o CSP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará S \_ OK.**

Se o método falhar, ele retornará um **valor HRESULT** que indica o erro. Para ver uma lista de códigos de erro comuns, consulte [Valores comuns de HRESULT.](common-hresult-values.md)

## <a name="remarks"></a>Comentários

A **função PvkGetCryptProv** primeiro tenta obter o handle do provedor do nome do contêiner de chave especificado pelo parâmetro *pwszKeyContainerName.* Se você passar **NULL** para o parâmetro *pwszKeyContainerName,* **PvkGetCryptProv** tentará obter o provedor do arquivo de chave privada especificado no parâmetro *pwszPvkFile.*

Quando terminar de usar o CSP, livre o handle do provedor e o contêiner de chave temporária chamando a [**função PvkFreeCryptProv.**](pvkfreecryptprov.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
