---
description: Use a API do Gerenciador de autorização para controlar o acesso aos recursos do aplicativo.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Usando a autorização em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753724"
---
# <a name="using-authorization-in-c"></a>Usando a autorização em C++

Você pode usar a API do Gerenciador de autorização para controlar o acesso aos recursos do aplicativo.

Se você tiver uma solução de controle de acesso com base nas [*listas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACLs) e quiser evitar a conversão dessa solução para usar o Gerenciador de autorização, poderá continuar a usar ACLs para controlar o acesso aos recursos. Para obter informações sobre como controlar o acesso a recursos usando ACLs, consulte [definindo permissões com ACLs em c++](defining-permissions-with-acls-in-c--.md), [estabelecendo um contexto de cliente de um SID em c++](establishing-a-client-context-from-a-sid-in-c--.md)e [verificando o acesso de cliente com ACLs em c++](verifying-client-access-with-acls-in-c--.md).

> [!Note]  
> Para grandes empresas, há uma compensação entre o desempenho e a sobrecarga administrativa. À medida que aumenta o número de recursos protegidos e os usuários, a administração das ACLs torna-se mais complicada. O desempenho não é afetado porque todas as informações necessárias sobre direitos de acesso são distribuídas para os recursos protegidos. O desempenho do Gerenciador de autorização é afetado pelo dimensionamento.

 

Para obter informações sobre outras tarefas de autorização, consulte [tarefas de suporte para autorização em C++](supporting-tasks-for-authorization-in-c--.md).



| Tópico                                                                                                                | Descrição                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definindo permissões em C++](defining-permissions-in-c--.md)                                                       | Defina quais usuários têm acesso a quais recursos de aplicativo Criando um repositório de política de autorização. |
| [Verificando o acesso do cliente a um recurso solicitado em C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Verifique se o cliente tem acesso a uma ou mais operações.                                           |
| [Delegando a definição de permissões em C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegar a administração de armazenamentos de diretiva de autorização armazenados no Active Directory.          |



 

 

 
