---
title: Assistentes de criação de objeto
description: Nos snap-ins administrativos do MMC de Active Directory Domain Services, o usuário pode criar novos objetos em um diretório abrindo o menu de contexto do contêiner em que o novo objeto será criado, escolhendo novo e escolhendo a classe de objeto a ser criada. A criação de novas instâncias de um objeto inicia o assistente para criação de objetos. Cada classe de objeto pode especificar o uso de um assistente de criação específico ou pode usar um assistente de criação genérico. Para classes comuns, como User e organizationalUnit, o snap-in Active Directory Users and Computers fornece um conjunto padrão de assistentes de criação. Há duas maneiras de estender um assistente de criação para substituir um assistente existente ou fornecer um caso não exista para a classe que o assistente existente é substituído por meio da criação de uma extensão de criação de objeto primário. Uma extensão de criação primária fornece o primeiro conjunto de páginas e é hospedada da mesma maneira que as páginas nativas. Uma extensão de criação primária também dá suporte ao mecanismo de extensibilidade para que outras extensões do assistente de criação possam ser invocadas. Para obter um exemplo de uma extensão primária, consulte o exemplo scpwizard no SDK (Software Development Kit) da plataforma. Estender um assistente existente um assistente existente pode ser estendido com uma extensão de criação de objeto secundário. Uma extensão de criação secundária adiciona páginas de assistente às páginas nativas ou à extensão primária. Para obter mais informações e um exemplo de uma extensão de criação secundária, consulte o exemplo de userwizard no SDK da plataforma.
ms.assetid: 7ac7ec21-72a9-4d1f-80f1-1eb5bfa2b296
ms.tgt_platform: multiple
keywords:
- ANÚNCIOS de objetos, assistentes de criação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc3dbacaf6eee5670fdacd9a587a497397c4d1b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084444"
---
# <a name="object-creation-wizards"></a>Assistentes de criação de objeto

Nos snap-ins administrativos do MMC de Active Directory Domain Services, o usuário pode criar novos objetos em um diretório abrindo o menu de contexto do contêiner em que o novo objeto será criado, escolhendo **novo** e escolhendo a classe de objeto a ser criada. A criação de novas instâncias de um objeto inicia o assistente para criação de objetos. Cada classe de objeto pode especificar o uso de um assistente de criação específico ou pode usar um assistente de criação genérico. Para classes comuns, como [**User**](/windows/desktop/ADSchema/c-user) e [**OrganizationalUnit**](/windows/desktop/ADSchema/c-organizationalunit), o snap-in Active Directory Users and Computers fornece um conjunto padrão de assistentes de criação.

Há duas maneiras de estender um assistente de criação:

-   Substitua um assistente existente ou forneça um se ele não existir para a classe: o assistente existente será substituído pela criação de uma *extensão de criação de objeto primário*. Uma extensão de criação primária fornece o primeiro conjunto de páginas e é hospedada da mesma maneira que as páginas nativas. Uma extensão de criação primária também dá suporte ao mecanismo de extensibilidade para que outras extensões do assistente de criação possam ser invocadas. Para obter um exemplo de uma extensão primária, consulte o exemplo scpwizard no SDK (Software Development Kit) da plataforma.
-   Estender um assistente existente: um assistente existente pode ser estendido com uma *extensão de criação de objeto secundário*. Uma extensão de criação secundária adiciona páginas de assistente às páginas nativas ou à extensão primária. Para obter mais informações e um exemplo de uma extensão de criação secundária, consulte o exemplo de userwizard no SDK da plataforma.

## <a name="developer-audience"></a>Público do desenvolvedor

Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++. No momento, não é possível criar uma extensão para o Active Directory assistente de criação de objeto usando Visual Basic.

## <a name="creating-an-active-directory-object-creation-extension"></a>Criando uma extensão de criação de objeto de Active Directory

As extensões de criação de objeto primário e secundário são servidores em processamento com que implementam determinadas interfaces e são registrados com Active Directory Domain Services.

**Para criar e instalar uma extensão de criação de objeto**

1.  Crie a DLL de extensão de criação de objeto. Uma extensão de criação de objeto é um servidor em processamento COM que, no mínimo, implementa a interface [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) . Para obter mais informações, consulte [implementando o objeto com da extensão de criação de objetos](implementing-the-object-creation-extension-com-object.md).
2.  Instale a extensão de criação em computadores em que a extensão de criação deve ser usada. Para fazer isso, crie um pacote de Microsoft Windows Installer para a DLL de extensão de criação e implante o pacote adequadamente usando a política de grupo. Para obter mais informações, consulte [distribuindo componentes da interface do usuário](distributing-user-interface-components.md).
3.  Registre a extensão de criação no registro do Windows e com Active Directory Domain Services. Para obter mais informações, consulte [registrando a extensão de criação de objeto](registering-the-object-creation-extension.md).

## <a name="using-an-object-creation-wizard"></a>Usando um assistente para criação de objetos

Um assistente de criação de objeto também pode ser invocado de um aplicativo diferente dos snap-ins administrativos do MMC de Active Directory Domain Services. Para obter mais informações, consulte [invocando assistentes de criação do seu aplicativo](invoking-creation-wizards-from-your-application.md).

Se um assistente de criação não estiver registrado para uma classe de objeto, os snap-ins administrativos fornecerão um assistente de criação genérico. O assistente de criação genérica é criado em tempo de execução na lista de propriedades obrigatórias para a classe de objeto criada. Para cada propriedade obrigatória, uma página é adicionada à interface do usuário. O assistente de criação genérica não é extensível. Se a extensibilidade for necessária, ela deverá ser substituída por uma extensão de criação de objeto primário.

 

 