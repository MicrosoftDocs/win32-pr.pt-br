---
description: Preterido. Recupera a chave no registro que corresponde a essa identidade de usuário.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Método IUserIdentity:: OpenIdentityRegKey (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967486"
---
# <a name="iuseridentityopenidentityregkey-method"></a>Método IUserIdentity:: OpenIdentityRegKey

\[O método **IUserIdentity:: OpenIdentityRegKey** está disponível para uso no Windows 2000. No Windows XP, essa funcionalidade foi substituída por [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md)e pode ser alterada ou indisponível nas versões subsequentes.\]

Preterido. Recupera a chave no registro que corresponde a essa identidade de usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDesiredAccess* \[ no\]
</dt> <dd>

Tipo: **DWORD**

Um valor que descreve o nível de acesso solicitado da chave do registro.

</dd> <dt>

*phKey* \[ fora\]
</dt> <dd>

Tipo: **HKEY \** _

Um ponteiro que recebe a chave do registro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

O resultado da solicitação do registro. Se for bem-sucedido, retornará **S \_ OK**. Caso contrário, ele retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_identidade E \_ não \_ encontrada**</dt> </dl> | Essa identidade não tem uma chave de registro associada.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>                 | A chave do registro não pôde ser acessada.<br/>             |



 

## <a name="remarks"></a>Comentários

O parâmetro *dwDesiredAccess* é um descritor de segurança de acesso do registro padrão que descreve o acesso que você deseja obter à chave do registro. Para obter mais informações sobre a segurança do registro, incluindo uma lista de valores aceitáveis para esse parâmetro, consulte [segurança da chave do registro e direitos de acesso](../sysinfo/registry-key-security-and-access-rights.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
