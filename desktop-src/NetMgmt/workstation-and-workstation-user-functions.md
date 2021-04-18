---
title: Funções de usuário da estação de trabalho e estação de trabalho
description: As funções de estação de trabalho de gerenciamento de rede executam tarefas administrativas em uma estação de trabalho local ou remota.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811825"
---
# <a name="workstation-and-workstation-user-functions"></a>Funções de usuário da estação de trabalho e estação de trabalho

As funções de estação de trabalho de gerenciamento de rede executam tarefas administrativas em uma estação de trabalho local ou remota. Somente um usuário ou aplicativo com associação de grupo de administradores, em um servidor local ou remoto, pode executar tarefas administrativas em uma estação de trabalho para controlar sua operação, acesso do usuário e compartilhamento de recursos. Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

As funções de estação de trabalho são listadas a seguir.



| Função                                   | Descrição                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Retorna informações sobre os elementos de configuração para uma estação de trabalho. |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Configura uma estação de trabalho.                                               |



 

As funções de estação de trabalho permitem o acesso a dois tipos discretos de informações de estação de trabalho:

-   Informações do sistema
-   Informações específicas da plataforma

Dentro de cada tipo, os dados são categorizados pelo acesso de segurança. Os dados acessíveis ao convidado são um subconjunto dos dados acessíveis pelo usuário, que, por sua vez, são um subconjunto dos dados acessíveis ao administrador.

As informações da estação de trabalho estão disponíveis nos seguintes níveis:

-   [**Informações de WKSTA \_ \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**Informações de WKSTA \_ \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**Informações de WKSTA \_ \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

As funções de usuário da estação de trabalho de gerenciamento de rede permitem acesso a informações específicas do usuário. As informações específicas do usuário são separadas das informações da estação de trabalho porque pode haver mais de um usuário em uma estação de trabalho.

As funções de usuário da estação de trabalho são listadas a seguir.



| Função                                           | Descrição                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Lista informações sobre todos os usuários conectados no momento à estação de trabalho.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Retorna informações sobre um usuário conectado no momento.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Define as informações específicas do usuário para os elementos de configuração de uma estação de trabalho. |



 

As informações de usuário da estação de trabalho estão disponíveis nos seguintes níveis:

-   [**Informações do usuário do WKSTA \_ \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**Informações de usuário do WKSTA \_ \_ \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**Informações do usuário do WKSTA \_ \_ \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 