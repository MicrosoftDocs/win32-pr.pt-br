---
title: Proteção de objeto e atributo
description: Uma ACL (lista de controle de acesso) protege todos os objetos no Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Proteção de objeto e atributo
- proteção de AD, objeto e atributo de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634933"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="4a36c-105">Proteção de objeto e atributo</span><span class="sxs-lookup"><span data-stu-id="4a36c-105">Object and Attribute Protection</span></span>

<span data-ttu-id="4a36c-106">Uma ACL (lista de controle de acesso) protege todos os objetos no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="4a36c-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="4a36c-107">As ACLs determinam quem pode exibir o objeto, quais atributos eles podem ler e quais ações cada usuário pode executar no objeto.</span><span class="sxs-lookup"><span data-stu-id="4a36c-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="4a36c-108">A existência de um objeto ou de um atributo nunca é revelada a um usuário não autorizado.</span><span class="sxs-lookup"><span data-stu-id="4a36c-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="4a36c-109">Uma ACL é uma lista de ACEs (entradas de controle de acesso) armazenadas com o objeto que ele protege.</span><span class="sxs-lookup"><span data-stu-id="4a36c-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="4a36c-110">No Windows NT e no Windows 2000, uma ACL é armazenada como um valor binário, chamado de descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="4a36c-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="4a36c-111">Cada ACE contém um SID (identificador de segurança), que identifica a entidade (usuário ou grupo) a quem a ACE se aplica e os dados sobre o tipo de acesso que a ACE concede ou nega.</span><span class="sxs-lookup"><span data-stu-id="4a36c-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="4a36c-112">As ACLs para objetos de diretório contêm ACEs que se aplicam ao objeto como um todo e as ACEs que se aplicam aos atributos individuais do objeto.</span><span class="sxs-lookup"><span data-stu-id="4a36c-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="4a36c-113">Isso permite que um administrador controle não apenas quais usuários podem ver um objeto, mas também quais propriedades esses usuários podem exibir.</span><span class="sxs-lookup"><span data-stu-id="4a36c-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="4a36c-114">Por exemplo, todos os usuários podem receber acesso de leitura aos atributos email e número de telefone para todos os outros usuários, mas as propriedades de segurança de usuários podem ser negadas a todos, exceto a membros de um grupo de administradores de segurança especial.</span><span class="sxs-lookup"><span data-stu-id="4a36c-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="4a36c-115">Os usuários individuais podem receber acesso de gravação a atributos pessoais, como o telefone e os endereços de email em seus próprios objetos de usuário.</span><span class="sxs-lookup"><span data-stu-id="4a36c-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




