---
description: A definição de interface ISCardAuth é fornecida como um padrão que pode ser seguido ao desenvolver um provedor de serviços de cartão inteligente. A interface ISCardAuth pode ser usada para expor os serviços de autenticação com suporte em um cartão inteligente.
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
ms.openlocfilehash: 55f92b06fb9c86c46ee0f9bf08350510ba4e6f897a95294a15265df7918de516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577846"
---
# <a name="iscardauth-interface"></a>Interface ISCardAuth

\[A **interface ISCardAuth** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

A definição de interface **ISCardAuth** é fornecida como um padrão que pode ser seguido ao desenvolver um provedor [*de serviços*](../secgloss/s-gly.md) de [*cartão inteligente*](../secgloss/c-gly.md).

A **interface ISCardAuth** pode ser usada para expor os serviços de autenticação com suporte em um cartão inteligente. Esses serviços incluem autenticação de aplicativo, autenticação de cartão inteligente e autenticação de usuário.

O exemplo a seguir mostra um uso típico da interface **ISCardAuth.**

**Para usar ISCardAuth**

1.  Crie uma **interface ISCardAuth** (por meio do método de interface [**ISCardManage**](iscardmanage.md) correspondente).
2.  Chame o método **ISCardAuth** apropriado [**(APP \_ Auth,**](iscardauth-app-auth.md) [**GetChallenge,**](iscardauth-getchallenge.md) [**ICC \_ Auth**](iscardauth-icc-auth.md)ou [**User \_ Auth).**](iscardauth-user-auth.md)
3.  Libere a **interface ISCardAuth.**

## <a name="members"></a>Membros

A **interface ISCardAuth** herda da interface [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardAuth** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface ISCardAuth** tem esses métodos.



| Método                                          | Descrição                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**APP \_ Auth**](iscardauth-app-auth.md)        | Permite que o aplicativo se autenttice usando um protocolo de desafio/assinatura.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Retorna um desafio do cartão inteligente.<br/>                                            |
| [**ICC \_ Auth**](iscardauth-icc-auth.md)        | Permite que um aplicativo autenture o cartão inteligente.<br/>                               |
| [**User \_ Auth**](iscardauth-user-auth.md)      | Permite o acesso aos serviços de autenticação de usuário.<br/>                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



 

 
