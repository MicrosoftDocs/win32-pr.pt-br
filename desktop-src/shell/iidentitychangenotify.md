---
description: Preterido. Fornece notificação de modificações para identidades de usuário no sistema, bem como solicitações de usuário para alternar a identidade do usuário atual.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interface IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4419f55b2fe4561a22035d962da5e3c271108d06fa417cfbed1b603c883e5b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721904"
---
# <a name="iidentitychangenotify-interface"></a>Interface IIdentityChangeNotify

\[a interface **IIdentityChangeNotify** está disponível para uso no Windows 2000. no Windows XP, essa funcionalidade foi substituída por [contas de usuário com troca rápida de usuário e Área de Trabalho Remota](fastuserswitching.md)e pode ser alterada ou indisponível nas versões subsequentes.\]

Preterido. Fornece notificação de modificações para identidades de usuário no sistema, bem como solicitações de usuário para alternar a identidade do usuário atual.

## <a name="members"></a>Membros

A interface **IIdentityChangeNotify** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IIdentityChangeNotify** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IIdentityChangeNotify** tem esses métodos.



| Método                                                                                 | Descrição                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | Preterido. Chamado quando informações sobre uma identidade de usuário são alteradas ou quando uma identidade de usuário é adicionada ou excluída.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | Preterido. Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | Preterido. Chamado quando as identidades de usuário são alternadas.<br/>                                                                      |



 

## <a name="remarks"></a>Comentários

Para implementar notificações, uma interface derivada deve se conectar ao [**IUserIdentityManager**](iuseridentitymanager.md) chamando [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) e passando um ponteiro para a interface.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
