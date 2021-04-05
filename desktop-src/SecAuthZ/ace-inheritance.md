---
description: Uma ACL de objetos pode conter ACEs herdadas de seu contêiner pai.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Herança de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921465"
---
# <a name="ace-inheritance"></a><span data-ttu-id="70aad-103">Herança de ACE</span><span class="sxs-lookup"><span data-stu-id="70aad-103">ACE Inheritance</span></span>

<span data-ttu-id="70aad-104">A ACL de um objeto pode conter ACEs herdadas de seu contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="70aad-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="70aad-105">Por exemplo, uma subchave do registro pode herdar ACEs da chave acima dela na hierarquia do registro.</span><span class="sxs-lookup"><span data-stu-id="70aad-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="70aad-106">Da mesma forma, um arquivo em um sistema de arquivos NTFS pode herdar ACEs do diretório que a contém.</span><span class="sxs-lookup"><span data-stu-id="70aad-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="70aad-107">A estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) de uma ACE contém um conjunto de sinalizadores de herança que controlam a herança de Ace e o efeito de uma ACE no objeto ao qual ele está anexado.</span><span class="sxs-lookup"><span data-stu-id="70aad-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="70aad-108">O sistema interpreta os sinalizadores de herança e outras informações de herança de acordo com as [regras de herança de Ace](ace-inheritance-rules.md).</span><span class="sxs-lookup"><span data-stu-id="70aad-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="70aad-109">Essas regras foram aprimoradas com os seguintes recursos:</span><span class="sxs-lookup"><span data-stu-id="70aad-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="70aad-110">Suporte para [propagação automática de ACEs herdáveis](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="70aad-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="70aad-111">Um sinalizador que diferencia as ACEs herdadas e as ACEs que foram aplicadas diretamente a um objeto.</span><span class="sxs-lookup"><span data-stu-id="70aad-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="70aad-112">ACEs específicas de objeto que permitem especificar o tipo de objeto filho que pode herdar a ACE.</span><span class="sxs-lookup"><span data-stu-id="70aad-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="70aad-113">A capacidade de impedir que uma DACL ou SACL herde ACEs Configurando os bits SE protegidos por \_ DACL \_ ou se \_ protegidos por SACL \_ nos bits de controle [*do descritor de segurança*](/windows/desktop/SecGloss/s-gly) , exceto para ACE de atributo de recurso do sistema \_ \_ \_ e \_ \_ Ace ID de política no escopo do sistema \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="70aad-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
