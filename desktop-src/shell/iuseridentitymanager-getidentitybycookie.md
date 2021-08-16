---
description: Não há suporte para GetIdentityByCookie e podem ser alterados ou não disponíveis no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuários e Área de Trabalho Remota.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: Método IUserIdentityManager::GetIdentityByCookie (Msident.h)
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
ms.openlocfilehash: a077f3e6a65a04e4c018198dde39b80c5a6e5acbee282c9e2cc282642526894b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678150"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>Método IUserIdentityManager::GetIdentityByCookie

\[**Não há suporte para GetIdentityByCookie** e podem ser alterados ou não disponíveis no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

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

*uidCookie* \[ Em\]
</dt> <dd>

Tipo: **\* GUID**

O endereço de um **valor guid** que representa o cookie para a identidade que você deseja recuperar.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

O endereço do ponteiro que receberá o objeto de identidade do usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

O resultado da solicitação de recuperação. Se for bem-sucedido, ele retornará S \_ OK. Caso contrário, retornará um dos códigos de erro a seguir.



| Código de retorno                                                                                            | Descrição                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**IDENTIDADE \_ E \_ NÃO \_ ENCONTRADA**</dt> </dl> | Não foi possível encontrar a identidade solicitada.<br/>     |
| <dl> <dt>**IDENTIDADES E \_ \_ DESABILITADAS**</dt> </dl> | O gerenciamento de identidades está desabilitado no sistema.<br/> |



 

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



 

 




