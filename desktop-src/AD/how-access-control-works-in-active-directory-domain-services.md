---
title: Como o controle de acesso funciona no Active Directory Domain Services
description: O controle de acesso para objetos no Active Directory Domain Services é baseado em modelos de controle de acesso do Windows NT e do Windows 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, segurança, descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917123"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Como o controle de acesso funciona no Active Directory Domain Services

O controle de acesso para objetos no Active Directory Domain Services é baseado em modelos de controle de acesso do Windows NT e do Windows 2000. Para obter mais informações e uma descrição detalhada desse modelo e de seus componentes, como descritores de segurança, tokens de acesso, SIDs, ACLs e ACEs, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).

Os privilégios de acesso para recursos em Active Directory Domain Services geralmente são concedidos por meio do uso de uma ACE (entrada de controle de acesso). Uma ACE define uma permissão de acesso ou auditoria em um objeto para um usuário ou grupo específico. Uma ACL (lista de controle de acesso) é a coleção ordenada de entradas de controle de acesso definidas para um objeto. Um descritor de segurança dá suporte a propriedades e métodos que criam e gerenciam ACLs. Para obter mais informações sobre modelos de segurança, consulte [segurança](/windows/desktop/SecAuthZ/access-control) ou o *Windows 2000 Server Resource Kit*. (Esse recurso pode não estar disponível em alguns idiomas e países ou regiões.)

A estrutura de tópicos básica do modelo de segurança é:

-   Descritor de segurança. Cada objeto de diretório tem seu próprio descritor de segurança que contém dados de segurança que protegem o objeto. O descritor de segurança pode conter uma DACL (lista de controle de acesso discricionário). Uma DACL contém uma lista de ACEs. Cada ACE concede ou nega um conjunto de direitos de acesso a um usuário ou grupo. Os direitos de acesso correspondem às operações, como leitura e gravação de propriedades, que podem ser executadas no objeto.
-   Contexto de segurança. Quando um objeto de diretório é acessado, o aplicativo especifica as credenciais da entidade de segurança que está fazendo a tentativa de acesso. Quando autenticado, essas credenciais determinam o contexto de segurança do aplicativo, que inclui as associações de grupo e os privilégios associados à entidade de segurança. Para obter mais informações sobre contextos de segurança, consulte [contextos de segurança e Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Verificação de acesso. O sistema concederá acesso a um objeto somente se o descritor de segurança do objeto conceder os direitos de acesso necessários à entidade de segurança que tenta a operação (ou a grupos aos quais a entidade de segurança pertence).

A tabela a seguir lista as interfaces ADSI usadas para manipular os recursos de controle de acesso do Active Directory Domain Services.



| Interface                                                 | Descrição                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Usado para ler e gravar propriedades de segurança de um objeto de serviço de diretório. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Usado para gerenciar e enumerar todas as ACEs para um objeto de serviço de diretório.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Usado para ler e gravar propriedades de ACE.                                    |



 

 

 