---
title: O que é um usuário
description: As contas de usuário são criadas e armazenadas como objetos no Active Directory Domain Services.
ms.assetid: da13d21a-1d8b-4d03-8880-7146e6fc4ba9
ms.tgt_platform: multiple
keywords:
- O que é um usuário Active Directory
- usuários Active Directory, o que é um usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c59b2ea46474860268f327bcd03d2ba67ecea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634903"
---
# <a name="what-is-a-user"></a>O que é um usuário?

As contas de usuário são criadas e armazenadas como objetos no Active Directory Domain Services. As contas de usuário podem ser usadas por usuários ou programas humanos, como os serviços do sistema usam para fazer logon em um computador. Quando um usuário faz logon, o sistema verifica a senha do usuário comparando-a com os dados armazenados no objeto de usuário do usuário no Active Directory Server. Se a senha for autenticada, ou seja, a senha apresentada corresponde à senha armazenada no objeto de usuário, o sistema produz um token de acesso. Um token de acesso é um objeto que descreve o contexto de segurança de um processo ou thread. Os dados em um token incluem a identidade de segurança e as associações de grupo da conta de usuário associada ao processo ou thread. Cada processo executado em nome desse usuário tem uma cópia desse token de acesso.

Cada usuário ou aplicativo que acessa recursos em um domínio do Windows deve ter uma conta no servidor de Active Directory. O Windows usa essa conta de usuário para verificar se o usuário ou aplicativo tem permissão para usar um recurso.

Uma conta de usuário pode ser usada para:

-   Permitir que usuários humanos façam logon em um computador e acessem recursos com base na identidade dessa conta de usuário.
-   Permitir que programas e serviços sejam executados em um contexto de segurança específico.
-   Gerencie o acesso do usuário a recursos compartilhados, como objetos e suas propriedades, compartilhamentos de rede, arquivos, diretórios, filas de impressora e assim por diante.

Os grupos podem conter membros, que são referências a usuários e a outros grupos. Os grupos também podem ser usados para controlar o acesso a recursos compartilhados. Ao atribuir permissões para recursos, por exemplo, compartilhamentos de arquivos, impressoras e assim por diante, os administradores devem atribuir essas permissões a um grupo em vez de aos usuários individuais. As permissões são atribuídas uma vez ao grupo, em vez de várias vezes para cada usuário individual. Isso ajuda a simplificar a manutenção e a administração de uma rede.

## <a name="users-compared-to-contacts"></a>Usuários comparados a contatos

Tanto os usuários quanto os contatos podem ser usados para representar usuários humanos. No entanto, um usuário é uma entidade de segurança; um contato não é.

Um usuário pode ser usado para permitir que um usuário humano faça logon e acesse recursos compartilhados.

Um contato é usado somente para fins de email e lista de distribuição. No entanto, um contato pode conter a maioria dos dados armazenados em um objeto de usuário, como endereço, números de telefone e assim por diante, porque o usuário e o contato são derivados do objeto **classSchema** Person. Um contato não tem nenhum contexto de segurança; Portanto, um contato não pode ser usado para controlar o acesso a recursos compartilhados e não pode ser usado para fazer logon em um computador.

## <a name="users-compared-to-computers"></a>Usuários comparados a computadores

A classe de objeto Computer herda da classe de objeto user. Um objeto de computador representa um computador; no entanto, o computador e os serviços locais do computador geralmente exigem acesso à rede e aos recursos compartilhados. Quando o computador acessa recursos compartilhados, e não o usuário conectado ao computador, ele precisa de um token de acesso exatamente como um usuário humano conectado como um usuário. Quando um computador acessa a rede, ele usa um token de acesso que contém o identificador de segurança para a conta de computador do computador e os grupos dos quais a conta é membro.

Um serviço pode ser executado no contexto de LocalSystem ou em uma conta de serviço específica. Em computadores que executam o Windows 2000, um serviço executado no contexto da conta LocalSystem usa as credenciais do computador.

 

 




