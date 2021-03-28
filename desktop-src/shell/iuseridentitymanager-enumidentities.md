---
description: 'IUserIdentityManager:: EnumIdentities não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'Método IUserIdentityManager:: EnumIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089713"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>Método IUserIdentityManager:: EnumIdentities

\[**IUserIdentityManager:: EnumIdentities** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Obtém um objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que pode ser usado para enumerar as identidades de usuário presentes no sistema.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnumUser* \[ fora\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

O endereço do ponteiro para o novo objeto de enumeração de identidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

O resultado da operação de recuperação. Se for bem-sucedido, retornará S \_ OK. Se o objeto de enumeração não puder ser criado, ele retornará E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método é útil para iteração na lista de identidades no sistema. Para recuperar uma única identidade por seu cookie sem acessar a lista, chame [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




