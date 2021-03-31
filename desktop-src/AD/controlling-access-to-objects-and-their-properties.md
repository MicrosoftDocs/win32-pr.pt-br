---
title: Controlando o acesso a objetos e suas propriedades
description: Para controlar o acesso a objetos de aplicativo, trabalhe com o descritor de segurança de objeto e, especificamente, com a DACL (lista de controle de acesso discricionário) e sua lista de ACEs (entradas de controle de acesso).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- AD de objeto, controlando o acesso ao
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159267"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>Controlando o acesso a objetos e suas propriedades

Para controlar o acesso a objetos de aplicativo, trabalhe com o descritor de segurança de objeto e, especificamente, com a DACL (lista de controle de acesso discricionário) e sua lista de ACEs (entradas de controle de acesso).

Quando um objeto é criado, ele recebe um descritor de segurança. Para obter mais informações e uma descrição das regras que o sistema usa para criar a DACL para um novo objeto, consulte [como descritores de segurança são definidos em novos objetos de diretório](how-security-descriptors-are-set-on-new-directory-objects.md). Essas regras revelam que você pode:

-   Crie um novo descritor de segurança e anexe-o ao objeto no momento da criação. Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto de diretório](creating-a-security-descriptor-for-a-new-directory-object.md).
-   Aplique uma ACE herdável, em qualquer ponto da hierarquia de diretório, de modo que uma ACE seja herdada por objetos na árvore. Um objeto pode herdar uma ACE de seu contêiner pai. Para obter mais informações, consulte [herança e delegação de administração](inheritance-and-delegation-of-administration.md).
-   Especifique uma ACE na DACL padrão no esquema, se você tiver os direitos de acesso necessários. Cada definição de classe de objeto no esquema inclui um descritor de segurança padrão que pode ter uma DACL padrão. Para obter mais informações, consulte [descritor de segurança padrão](default-security-descriptor.md).

Além disso, a DACL de um objeto existente pode ser modificada. Você pode:

-   Substitua a DACL por uma nova.
-   Leia a DACL existente, modifique-a e aplique a DACL modificada. Para obter mais informações, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).

A lista a seguir descreve a função mais importante de uma ACE no Active Directory Domain Services. Com uma ACE, você pode:

-   Controle quem pode executar operações específicas em um objeto.
-   Controle quem tem acesso a uma propriedade específica ou a um conjunto de propriedades de um objeto.
-   Controle quem pode criar objetos filho em um contêiner, incluindo quem pode criar um tipo específico de objeto filho.
-   Defina controle privado-direitos de acesso para um tipo de objeto e controle quem pode executar as operações protegidas pelos direitos particulares.
-   Aplique uma ACE a um objeto de contêiner na raiz de uma subárvore de diretório, de modo que as proteções possam ser herdadas automaticamente por todos os objetos filho na árvore.
-   Aplicar uma ACE que é herdada automaticamente por um tipo específico de objeto filho em uma subárvore.
-   Crie uma ACE que conceda direitos a um grupo de segurança, e não a um único usuário.
-   Aplique uma ACE a Política de Grupo objetos para controlar as contas e os computadores afetados pela política.

 

 




