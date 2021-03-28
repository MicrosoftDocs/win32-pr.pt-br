---
description: GetIdentityByCookie não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Método IUserIdentityManager:: GetIdentityByCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501147"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>Método IUserIdentityManager:: GetIdentityByCookie

\[**GetIdentityByCookie** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Obtém uma identidade de usuário específica pelo cookie usado para identificá-la exclusivamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uidCookie* \[ no\]
</dt> <dd>

Tipo: **GUID \** _

O endereço de um valor _ *GUID** que representa o cookie para a identidade que você deseja recuperar.

</dd> <dt>

*ppIdentity* \[ fora\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

O endereço do ponteiro que receberá o objeto de identidade do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

O resultado da solicitação de recuperação. Se for bem-sucedido, retornará S \_ OK. Caso contrário, ele retornará um dos seguintes códigos de erro.



| Código de retorno                                                                                            | Description                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_identidade E \_ não \_ encontrada**</dt> </dl> | Não foi possível encontrar a identidade solicitada.<br/>     |
| <dl> <dt>**\_identidades E \_ desabilitadas**</dt> </dl> | O gerenciamento de identidades está desabilitado no sistema.<br/> |



 

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



 

 




