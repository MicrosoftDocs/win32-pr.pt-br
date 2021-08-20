---
description: Não há suporte para IUserIdentityManager e pode ser alterado ou não disponível no futuro. Em vez disso, use Contas de Usuário com Troca rápida de usuários e Área de Trabalho Remota.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interface IUserIdentityManager (Msident.h)
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
ms.openlocfilehash: 3181677df73d2976853d373c2ec4b9ec24d321151598bf77acdc4ffbaa17508f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049559"
---
# <a name="iuseridentitymanager-interface"></a>Interface IUserIdentityManager

\[**Não há suporte para IUserIdentityManager** e pode ser alterado ou não disponível no futuro. Em vez disso, [use Contas de Usuário com a Opção de](fastuserswitching.md)Usuário Rápida e Área de Trabalho Remota .\]

Expõe métodos que identificam, enumeram e gerenciam identidades de usuário no sistema.

## <a name="members"></a>Membros

A interface **IUserIdentityManager** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IUserIdentityManager** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IUserIdentityManager** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Entidades EnumId**](iuseridentitymanager-enumidentities.md)           | Preterido. Obtém [**um objeto IEnumUserIdentity,**](ienumuseridentity.md) que pode ser usado para enumerar por meio das identidades de usuário presentes no sistema.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | Preterido. Obtém uma identidade de usuário específica pelo cookie usado para identificá-la exclusivamente.<br/>                                                                        |
| [**Logoff**](iuseridentitymanager-logoff.md)                           | Preterido. Faça logoff da identidade atual.<br/>                                                                                                                    |
| [**Logon**](iuseridentitymanager-logon.md)                             | Preterido. Exibe uma interface do usuário para o usuário, permitindo que o usuário escolha uma identidade de usuário. Se for bem-sucedida, a identidade do usuário será registrada e recuperada.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | Preterido. Exibe uma interface do usuário para o usuário, permitindo que o usuário gerencie identidades de usuário.<br/>                                                                          |



 

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
