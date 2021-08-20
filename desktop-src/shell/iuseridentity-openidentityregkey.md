---
description: Preterido. Recupera a chave no Registro que corresponde a essa identidade de usuário.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: Método IUserIdentity::OpenIdentityRegKey (Msident.h)
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
ms.openlocfilehash: 89b80162b558222e1dc3e8caf518042ac90700ae7f7bde82b1b235111c9bdb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678430"
---
# <a name="iuseridentityopenidentityregkey-method"></a>Método IUserIdentity::OpenIdentityRegKey

\[O **método IUserIdentity::OpenIdentityRegKey** está disponível para uso no Windows 2000. No Windows XP, essa funcionalidade foi superada por Contas de Usuário com a Troca Rápida de Usuários [e](fastuserswitching.md)Área de Trabalho Remota e pode ser alterada ou não disponível nas versões subsequentes.\]

Preterido. Recupera a chave no Registro que corresponde a essa identidade de usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDesiredAccess* \[ Em\]
</dt> <dd>

Tipo: **DWORD**

Um valor que descreve o nível de acesso solicitado da chave do Registro.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Tipo: **HKEY \***

Um ponteiro que recebe a chave do Registro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

O resultado da solicitação do Registro. Se for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                            | Descrição                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**IDENTIDADE \_ E \_ NÃO \_ ENCONTRADA**</dt> </dl> | Essa identidade não tem uma chave do Registro associada.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                 | A chave do Registro não pôde ser acessada.<br/>             |



 

## <a name="remarks"></a>Comentários

O *parâmetro dwDesiredAccess* é um descritor de segurança de acesso do Registro padrão que descreve o acesso que você deseja obter à chave do Registro. Para obter mais informações sobre a segurança do Registro, incluindo uma lista de valores aceitáveis para esse parâmetro, consulte Direitos de acesso e segurança de chave [do Registro.](../sysinfo/registry-key-security-and-access-rights.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
