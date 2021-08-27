---
description: Não há suporte para GetIdentityFolder e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuários e Área de Trabalho Remota.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: Método IUserIdentity::GetIdentityFolder (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 20357dde27214177a454eb585dcd51182228c247da5aeae5ef887089b73ed85d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720602"
---
# <a name="iuseridentitygetidentityfolder-method"></a>Método IUserIdentity::GetIdentityFolder

\[**Não há suporte para GetIdentityFolder** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Obtém a pasta de arquivo associada a essa identidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Obrigatórios. Um valor que especifica se a pasta associada a essa identidade é roaming. Deve ser um dos valores a seguir.

<dt>



 (GIF \_ PASTA \_ ROAMING)


</dt> <dd>

A pasta está em roaming.

</dd> <dt>



 (GIF \_ PASTA \_ NÃO \_ ROAMING)


</dt> <dd>

A pasta é local.

</dd> </dl> </dd> <dt>

*pszPath* \[ Em\]
</dt> <dd>

Tipo: **WCHAR \***

Um ponteiro para uma cadeia de caracteres largos que recebe o caminho da pasta.

</dd> <dt>

*ulBuffSize* \[ Em\]
</dt> <dd>

Tipo: **ULONG**

Um valor que especifica o tamanho de *pszPath.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte ao servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




