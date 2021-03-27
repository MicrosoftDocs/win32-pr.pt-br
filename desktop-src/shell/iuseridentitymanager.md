---
description: IUserIdentityManager não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interface IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826721"
---
# <a name="iuseridentitymanager-interface"></a>Interface IUserIdentityManager

\[**IUserIdentityManager** não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]

Expõe métodos que identificam, enumeram e gerenciam identidades de usuário no sistema.

## <a name="members"></a>Membros

A interface **IUserIdentityManager** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentityManager** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUserIdentityManager** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | Preterido. Obtém um objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que pode ser usado para enumerar as identidades de usuário presentes no sistema.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | Preterido. Obtém uma identidade de usuário específica pelo cookie usado para identificá-la exclusivamente.<br/>                                                                        |
| [**Verbos**](iuseridentitymanager-logoff.md)                           | Preterido. Faça logoff da identidade atual.<br/>                                                                                                                    |
| [**Logon**](iuseridentitymanager-logon.md)                             | Preterido. Exibe uma IU para o usuário, permitindo que o usuário escolha uma identidade de usuário. Se for bem-sucedido, a identidade do usuário será registrada e recuperada.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | Preterido. Exibe uma IU para o usuário, permitindo que o usuário gerencie identidades de usuário.<br/>                                                                          |



 

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
