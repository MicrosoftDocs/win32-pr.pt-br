---
title: Herança e delegação de administração
description: Descreve AD DS suporte para a herança de permissões na árvore de objetos e também herança específica de objeto.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- herança de administração e delegação Active Directory
- Active Directory Active Directory, herança de permissões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b48ff4d913cbd8bf16f7b2c67adf86d61515298dcac267291641d30504e1e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187519"
---
# <a name="inheritance-and-delegation-of-administration"></a>Herança e delegação de administração

Active Directory Domain Services dá suporte à herança de permissões na árvore de objetos para permitir que as tarefas de administração sejam executadas em níveis mais altos na árvore. Isso permite que os administradores configurem permissões herdáveis em objetos próximos à raiz, como domínio e unidades organizacionais, e tenham essas permissões distribuídas a vários objetos na árvore.

A herança pode ser definida em uma base por ACE. A tabela a seguir lista os sinalizadores que podem ser especificados no **AceFlags** para controlar a herança da Ace.



| Sinalizador                                                     | Descrição                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE de \_ herança de ACEFLAG ADS \_**<br/>                | Faz com que a ACE seja herdada na árvore.<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ não \_ propagar \_ a \_ Ace INHERIT**<br/> | Faz com que a ACE seja herdada apenas um nível na árvore.<br/>                                                                      |
| **os anúncios \_ ACEFLAG \_ herdam \_ apenas \_ Ace**<br/>          | Faz com que a ACE seja ignorada no objeto no qual ela está especificada, seja herdada somente e seja efetiva onde foi herdada.<br/> |



 

Além de definir a herança, o Active Directory Domain Services dá suporte à herança específica do objeto. Isso permite que as ACEs herdáveis sejam herdadas para baixo na árvore, mas entram em vigor apenas em um tipo específico de objeto. Isso é extremamente útil na delegação da administração. Por exemplo, isso pode ser usado para definir uma ACE herdável específica de objeto em uma unidade organizacional que permite que um grupo tenha controle total sobre todos os objetos de usuário na unidade organizacional, mas nada mais. Assim, o gerenciamento de usuários nessa unidade organizacional é delegado aos usuários nesse grupo.

### <a name="delegating-service-administration-with-security-groups"></a>Delegando a administração do serviço com grupos de segurança

Use grupos de segurança para definir e delegar funções administrativas associadas ao servidor de aplicativos. Por exemplo, seu serviço pode estar associado a um grupo Administradores de myatendimento. Os usuários identificados como administradores do MyService serão adicionados ao grupo de administradores do MyService. O programa de instalação do MyService pode definir ACLs no diretório para habilitar os administradores de MyService permissões suficientes para ler/gravar atributos relacionados a MyService ou criar objetos específicos de MyService, por exemplo.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Funções em grupos de segurança para computadores que executam seu serviço

Use grupos de segurança para definir o conjunto de computadores que recebem acesso aos objetos do serviço no diretório. Por exemplo, seu serviço pode estar associado a um grupo de servidores MyService. Todos os computadores que executam o servidor MyService são adicionados ao grupo de servidores MyService e esse grupo pode receber acesso a partes do diretório em que os servidores de MyService precisam ler/gravar dados. O programa de instalação do MyService pode definir ACLs no diretório para habilitar os servidores de MyService permissões suficientes para ler/gravar atributos relacionados a MyService ou criar objetos específicos de MyService, por exemplo.

 

 





