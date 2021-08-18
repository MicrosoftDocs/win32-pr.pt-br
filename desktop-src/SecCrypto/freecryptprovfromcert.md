---
description: Libera o alça para um CSP (provedor de serviços criptográficos) e, opcionalmente, exclui o contêiner temporário criado pela função GetCryptProvFromCert.
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
ms.openlocfilehash: 8797a6f48bcfb973a6c07a4b05ae0d39bc3b4522ab6f7ae70a80eaa77081da44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006784"
---
# <a name="freecryptprovfromcert-function"></a>Função FreeCryptProvFromCert

> [!IMPORTANT]
> Essa API está preterida. A Microsoft pode remover essa API em versões futuras.

 

A **função FreeCryptProvFromCert** libera [*o*](../secgloss/c-gly.md) alça para um CSP (provedor de serviços de criptografia) e, opcionalmente, exclui o contêiner temporário criado pela função [**GetCryptProvFromCert.**](getcryptprovfromcert.md)

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

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

*fAcquired* \[ Em\]
</dt> <dd>

Um valor que especifica se o handle do provedor foi adquirido do [*certificado*](../secgloss/c-gly.md).

</dd> <dt>

*hProv* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura HCRYPTPROV**](hcryptprov.md) para o CSP.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
