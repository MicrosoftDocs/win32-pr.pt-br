---
description: Libera o identificador para um CSP (provedor de serviços de criptografia) e, opcionalmente, exclui o contêiner temporário criado pela função PvkGetCryptProv.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Função PvkFreeCryptProv
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796371"
---
# <a name="pvkfreecryptprov-function"></a>Função PvkFreeCryptProv

> [!IMPORTANT]
> Essa API está preterida. A Microsoft poderá remover essa API em versões futuras.

 

A função **PvkFreeCryptProv** libera o identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e, opcionalmente, exclui o contêiner temporário criado pela função [**PvkGetCryptProv**](pvkgetcryptprov.md) .

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProv* \[ no\]
</dt> <dd>

Um identificador para o CSP.

</dd> <dt>

*pwszCapiProvider* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome do CSP.

</dd> <dt>

*dwProviderType* \[ no\]
</dt> <dd>

Um valor **DWORD** que representa o tipo de provedor criptográfico. Para obter mais informações, consulte [tipos de provedor criptográfico](cryptographic-provider-types.md).

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



 

 
