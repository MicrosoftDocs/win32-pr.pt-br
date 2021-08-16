---
title: Como o controle de acesso funciona Active Directory Domain Services
description: O controle de acesso para objetos Active Directory Domain Services é baseado em Windows NT e Windows de controle de acesso 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, segurança, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f53cdd7b958313b3cb16bc538addc73b42bd0dc917160176422b85c959c8c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188282"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Como o controle de acesso funciona Active Directory Domain Services

O controle de acesso para objetos Active Directory Domain Services é baseado em Windows NT e Windows de controle de acesso 2000. Para obter mais informações e uma descrição detalhada desse modelo e seus componentes, como descritores de segurança, tokens de acesso, SIDs, ACLs e ACEs, consulte [Modelo](/windows/desktop/SecAuthZ/access-control-model)de Controle de Acesso .

Os privilégios de acesso para recursos Active Directory Domain Services em geral são concedidos por meio do uso de uma ACE (entrada de controle de acesso). Uma ACE define uma permissão de acesso ou auditoria em um objeto para um usuário ou grupo específico. Uma ACL (lista de controle de acesso) é a coleção ordenada de entradas de controle de acesso definidas para um objeto . Um descritor de segurança dá suporte a propriedades e métodos que criam e gerenciam ACLs. Para obter mais informações sobre modelos de segurança, consulte [Security](/windows/desktop/SecAuthZ/access-control) *ou Windows 2000 Server Resource Kit*. (Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)

A estrutura básica do modelo de segurança é:

-   Descritor de segurança. Cada objeto de diretório tem seu próprio descritor de segurança que contém dados de segurança que protegem o objeto. O descritor de segurança pode conter uma DACL (lista de controle de acesso discricionário). Uma DACL contém uma lista de ACEs. Cada ACE concede ou nega um conjunto de direitos de acesso a um usuário ou grupo. Os direitos de acesso correspondem às operações, como ler e escrever propriedades, que podem ser executadas no objeto .
-   Contexto de segurança. Quando um objeto de diretório é acessado, o aplicativo especifica as credenciais da entidade de segurança que está fazendo a tentativa de acesso. Quando autenticadas, essas credenciais determinam o contexto de segurança do aplicativo, que inclui as associações de grupo e os privilégios associados à entidade de segurança. Para obter mais informações sobre contextos de segurança, consulte [Contextos de segurança e Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Verificação de acesso. O sistema concede acesso a um objeto somente se o descritor de segurança do objeto concede os direitos de acesso necessários à entidade de segurança que está tentando a operação (ou a grupos aos quais a entidade de segurança pertence).

A tabela a seguir lista as interfaces ADSI usadas para manipular os recursos de controle de acesso Active Directory Domain Services.



| Interface                                                 | Descrição                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Usado para ler e gravar propriedades de segurança de um objeto de serviço de diretório. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Usado para gerenciar e enumerar todas as ACEs para um objeto de serviço de diretório.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Usado para ler e gravar propriedades ACE.                                    |



 

 

 