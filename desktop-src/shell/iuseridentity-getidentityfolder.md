---
description: GetIdentityFolder não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Método IUserIdentity:: GetIdentityFolder (Msident. h)'
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
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967488"
---
# <a name="iuseridentitygetidentityfolder-method"></a>Método IUserIdentity:: GetIdentityFolder

\[**GetIdentityFolder** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Obtém a pasta de arquivos associada a essa identidade.

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

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Obrigatórios. Um valor que especifica se a pasta associada a essa identidade está em roaming. Deve ser um dos valores a seguir.

<dt>



 (GIF \_ pasta de ROAMing \_ )


</dt> <dd>

A pasta está em roaming.

</dd> <dt>



 (GIF \_ \_pasta não móvel \_ )


</dt> <dd>

A pasta é local.

</dd> </dl> </dd> <dt>

*pszPath* \[ no\]
</dt> <dd>

Tipo: **WCHAR \** _

Um ponteiro para uma cadeia de caracteres largos que recebe o caminho da pasta.

</dd> <dt>

_ulBuffSize * \[ in\]
</dt> <dd>

Tipo: **ULONG**

Um valor que especifica o tamanho de *pszPath*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fim do suporte do servidor<br/>    | Windows 2000 Server<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




