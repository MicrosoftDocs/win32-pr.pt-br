---
title: Delegação
description: A delegação é um dos recursos de segurança mais importantes do Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- ANÚNCIO de delegação
- ANÚNCIO de segurança, delegação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915957"
---
# <a name="delegation"></a><span data-ttu-id="7fa81-105">Delegação</span><span class="sxs-lookup"><span data-stu-id="7fa81-105">Delegation</span></span>

<span data-ttu-id="7fa81-106">A *delegação* é um dos recursos de segurança mais importantes do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="7fa81-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="7fa81-107">A delegação permite que uma autoridade administrativa mais alta Conceda direitos administrativos específicos para contêineres e subárvores a indivíduos e grupos.</span><span class="sxs-lookup"><span data-stu-id="7fa81-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="7fa81-108">Os administradores de domínio, com autoridade ampla sobre grandes segmentos de usuários, não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="7fa81-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="7fa81-109">Uma ACE pode conceder direitos administrativos específicos para os objetos em um contêiner para um usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="7fa81-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="7fa81-110">São concedidos direitos para operações específicas em classes de objetos específicas usando ACEs na ACL do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7fa81-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="7fa81-111">Por exemplo, para habilitar um usuário chamado "usuário 1" para ser um administrador da unidade organizacional "contabilidade corporativa", adicione ACEs à ACL em "contabilidade corporativa" da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7fa81-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="7fa81-112">"usuário 1"; Conceder Criar, modificar, excluir; usuário de classe de objeto "usuário 1"; Conceder Criar, modificar, excluir; grupo de classes de objeto "usuário 1"; Conceder Write; usuário de classe de objeto; Senha do atributo "</span><span class="sxs-lookup"><span data-stu-id="7fa81-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="7fa81-113">Agora, o usuário 1 pode criar novos usuários e grupos em contabilidade corporativa e definir as senhas em usuários existentes, mas o usuário 1 não pode criar nenhuma outra classe de objeto e não pode afetar os usuários em nenhum outro contêiner, a menos que, é claro, o usuário 1 receba esse acesso por ACEs nos outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="7fa81-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




