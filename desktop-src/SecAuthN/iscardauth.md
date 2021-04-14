---
description: A definição da interface ISCardAuth é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um provedor de serviços de cartão inteligente. A interface ISCardAuth pode ser usada para expor os serviços de autenticação com suporte por um cartão inteligente.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interface ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461060"
---
# <a name="iscardauth-interface"></a>Interface ISCardAuth

\[A interface **ISCardAuth** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição da interface **ISCardAuth** é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviços*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .

A interface **ISCardAuth** pode ser usada para expor os serviços de autenticação com suporte por um cartão inteligente. Esses serviços incluem autenticação de aplicativo, autenticação de cartão inteligente e autenticação de usuário.

O exemplo a seguir mostra um uso típico da interface **ISCardAuth** .

**Para usar o ISCardAuth**

1.  Crie uma interface **ISCardAuth** (por meio do método de interface [**ISCardManage**](iscardmanage.md) correspondente).
2.  Chame o método **ISCardAuth** apropriado ([**app \_ auth**](iscardauth-app-auth.md), [**Getchallenge**](iscardauth-getchallenge.md), [**ICC \_ auth**](iscardauth-icc-auth.md)ou [**user \_ auth**](iscardauth-user-auth.md)).
3.  Libere a interface **ISCardAuth** .

## <a name="members"></a>Membros

A interface **ISCardAuth** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardAuth** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISCardAuth** tem esses métodos.



| Método                                          | Descrição                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Autenticação de aplicativo \_**](iscardauth-app-auth.md)        | Permite que o aplicativo se autentique usando um protocolo de desafio/assinatura.<br/> |
| [**Getchallenge**](iscardauth-getchallenge.md) | Retorna um desafio do cartão inteligente.<br/>                                            |
| [**\_Autenticação ICC**](iscardauth-icc-auth.md)        | Permite que um aplicativo autentique o cartão inteligente.<br/>                               |
| [**Autenticação do usuário \_**](iscardauth-user-auth.md)      | Permite o acesso aos serviços de autenticação de usuário.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



 

 
