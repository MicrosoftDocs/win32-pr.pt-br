---
description: Cria um contêiner temporário no CSP (provedor de serviços de criptografia) e carrega uma chave privada da memória no contêiner.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: Função PvkPrivateKeyAcquireContextFromMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297346"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a>Função PvkPrivateKeyAcquireContextFromMemory

> [!IMPORTANT]
> Essa API está preterida. A Microsoft poderá remover essa API em versões futuras.

 

A função **PvkPrivateKeyAcquireContextFromMemory** cria um contêiner temporário no CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e carrega uma [*chave privada*](../secgloss/p-gly.md) da memória no contêiner.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszProvName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do CSP cujo tipo é solicitado em *dwProvType*.

</dd> <dt>

*dwProvType* \[ no\]
</dt> <dd>

Um valor **DWORD** para o tipo CSP. Para obter mais informações sobre tipos de CSP, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[ no\]
</dt> <dd>

Um ponteiro para um buffer para receber os dados de contexto. O chamador deve fornecer esse recurso.

</dd> <dt>

*cbData* \[ no\]
</dt> <dd>

Um valor **DWORD** que especifica o tamanho, em bytes, do buffer *pbData* . O chamador deve fornecer esse valor.

</dd> <dt>

*hwndOwner* \[ no\]
</dt> <dd>

Se uma senha for necessária para descriptografar os dados de contexto apontados pelo parâmetro *pbData* , esse parâmetro será um identificador para o pai da caixa de diálogo; caso contrário, será **nulo**.

</dd> <dt>

*pwszKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da chave a ser recuperada.

</dd> <dt>

*pdwKeySpec* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para um valor **DWORD** que especifica o tipo de chave. Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.

</dd> <dt>

*phCryptProv* \[ fora\]
</dt> <dd>

Um ponteiro para um identificador para o CSP.

</dd> <dt>

*ppwszTmpContainer* \[ fora\]
</dt> <dd>

O endereço de um ponteiro para uma cadeia de caracteres terminada em nulo para o nome de contêiner temporário. A função **PvkPrivateKeyAcquireContextFromMemory** fornece o buffer para essa cadeia de caracteres e a inicializa. Ao chamar **PvkPrivateKeyAcquireContextFromMemory**, o endereço deve apontar para um valor **nulo** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Após o êxito, essa função retornará **true**. A função **PvkPrivateKeyAcquireContextFromMemory** retornará **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
