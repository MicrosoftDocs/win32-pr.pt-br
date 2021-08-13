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
> Essa API está preterida. A Microsoft pode remover essa API em versões futuras.

 

A **função PvkPrivateKeySave** [](../secgloss/p-gly.md) salva uma chave privada e sua chave [*pública correspondente*](../secgloss/p-gly.md) em um arquivo especificado.

> [!Note]  
> Essa função não tem nenhum arquivo de header associado ou biblioteca de importação. Para chamar essa função, você deve criar um arquivo de título definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente ao Mssign32.dll.

 

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

*hCryptProv* \[ Em\]
</dt> <dd>

Um handle para um [*CSP (provedor de serviços*](../secgloss/c-gly.md) criptográficos).

</dd> <dt>

*hFile* \[ Em\]
</dt> <dd>

Um handle para um arquivo criado com permissão inicial de leitura/gravação e permissão subsequente somente leitura.

</dd> <dt>

*dwKeySpec* \[ Em\]
</dt> <dd>

Um inteiro longo para o tipo de chave. Os valores possíveis **\_ incluem AT KEYEXCHANGE** **ou AT \_ SIGNATURE.**

</dd> <dt>

*hwndOwner* \[ Em\]
</dt> <dd>

Se uma senha for necessária para criptografar a chave privada, esse parâmetro será um indicador para o pai da caixa de diálogo; caso contrário, será **NULL.**

</dd> <dt>

*pwszKeyName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo para o nome da chave a ser salva.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Um **valor DWORD** que especifica opções adicionais para a função. Para obter mais informações, consulte *o parâmetro dwFlags* [**em CryptExportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Após o sucesso, essa função retorna **TRUE.** A **função PvkPrivateKeySave** retornará **FALSE** se falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
