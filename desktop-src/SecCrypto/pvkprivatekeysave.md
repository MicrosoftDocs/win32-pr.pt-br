---
description: Salva uma chave privada e sua chave pública correspondente em um arquivo especificado.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Função PvkPrivateKeySave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 3a2eed4b907f7c22414634a4b1ef49df6ca780181109a7396de2f8aa1776b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901205"
---
# <a name="pvkprivatekeysave-function"></a>Função PvkPrivateKeySave

> [!IMPORTANT]
> Essa API está preterida. A Microsoft poderá remover essa API em versões futuras.

 

A função **PvkPrivateKeySave** salva uma [*chave privada*](../secgloss/p-gly.md) e sua [*chave pública*](../secgloss/p-gly.md) correspondente em um arquivo especificado.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HCRYPTPROV* \[ no\]
</dt> <dd>

Um identificador para um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).

</dd> <dt>

*hFile* \[ no\]
</dt> <dd>

Um identificador para um arquivo criado com a permissão de leitura/gravação inicial e a permissão de somente leitura subsequente.

</dd> <dt>

*dwKeySpec* \[ no\]
</dt> <dd>

Um inteiro longo para o tipo de chave. Os valores possíveis incluem **em \_ keyexchange** ou **na \_ assinatura**.

</dd> <dt>

*hwndOwner* \[ no\]
</dt> <dd>

Se uma senha for necessária para criptografar a chave privada, esse parâmetro será um identificador para o pai da caixa de diálogo; caso contrário, será **nulo**.

</dd> <dt>

*pwszKeyName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome da chave a ser salva.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um valor **DWORD** que especifica opções adicionais para a função. Para obter mais informações, consulte o parâmetro *dwFlags* em [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Após o êxito, essa função retornará **true**. A função **PvkPrivateKeySave** retornará **false** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
