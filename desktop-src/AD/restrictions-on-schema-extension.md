---
title: Restrições na extensão do esquema
description: Para reduzir a possibilidade de alterações de esquema em um aplicativo que está interrompendo outros aplicativos e manter a consistência do esquema, Active Directory Domain Services impor restrições sobre o tipo de alterações de esquema que um aplicativo ou usuário tem permissão para fazer.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634924"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="a6888-103">Restrições na extensão do esquema</span><span class="sxs-lookup"><span data-stu-id="a6888-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="a6888-104">Para reduzir a possibilidade de alterações de esquema em um aplicativo que está interrompendo outros aplicativos e manter a consistência do esquema, Active Directory Domain Services impor restrições sobre o tipo de alterações de esquema que um aplicativo ou usuário tem permissão para fazer.</span><span class="sxs-lookup"><span data-stu-id="a6888-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="a6888-105">As restrições são impostas apenas na modificação de objetos de esquema existentes.</span><span class="sxs-lookup"><span data-stu-id="a6888-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="a6888-106">O esquema é categorizado em duas categorias.</span><span class="sxs-lookup"><span data-stu-id="a6888-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="a6888-107">Os objetos de esquema que acompanham o Windows 2000 no esquema base pertencem à categoria 1.</span><span class="sxs-lookup"><span data-stu-id="a6888-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="a6888-108">Todos os objetos de esquema adicionados posteriormente por outros aplicativos ou usuários por meio da extensão de esquema dinâmico pertencem à categoria 2.</span><span class="sxs-lookup"><span data-stu-id="a6888-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="a6888-109">A categoria de um objeto de esquema pode ser determinada pelo conjunto de bits 0x10 definido no atributo **systemFlags** no objeto **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="a6888-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="a6888-110">Esse bit só é definido na categoria 1 objetos e não pode ser alterado, nem pode ser definido em qualquer objeto Category 2.</span><span class="sxs-lookup"><span data-stu-id="a6888-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="a6888-111">O atributo **systemFlags** é usado internamente pelo Active Directory Domain Services para identificar características especiais de objetos de "infraestrutura" no esquema de base.</span><span class="sxs-lookup"><span data-stu-id="a6888-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="a6888-112">Além de identificar objetos da categoria 1, **systemFlags** controla se um objeto pode ser movido, excluído ou renomeado.</span><span class="sxs-lookup"><span data-stu-id="a6888-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="a6888-113">Essas operações são impedidas para objetos que o Windows 2000 depende para serem executados.</span><span class="sxs-lookup"><span data-stu-id="a6888-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="a6888-114">Em qualquer objeto de esquema, categoria 1 ou 2, Active Directory Domain Services impor as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="a6888-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="a6888-115">Você não pode adicionar um novo **mustContain** a uma classe (diretamente ou por meio de herança adicionando uma classe auxiliar).</span><span class="sxs-lookup"><span data-stu-id="a6888-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="a6888-116">Não é possível excluir qualquer **mustContain** da classe (diretamente ou por meio de herança).</span><span class="sxs-lookup"><span data-stu-id="a6888-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="a6888-117">Além disso, as seguintes restrições adicionais são impostas em objetos de esquema da categoria 1:</span><span class="sxs-lookup"><span data-stu-id="a6888-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="a6888-118">Você não pode alterar os seguintes atributos de um atributo category 1:</span><span class="sxs-lookup"><span data-stu-id="a6888-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="a6888-119">**RangeLower** e **rangeUpper** (intervalo de valores).</span><span class="sxs-lookup"><span data-stu-id="a6888-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="a6888-120">**attributeSecurityGuid** (determina a qual conjunto de propriedades o atributo pertence, se houver).</span><span class="sxs-lookup"><span data-stu-id="a6888-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="a6888-121">Não é possível alterar o **defaultObjectCategory** de uma classe Category 1.</span><span class="sxs-lookup"><span data-stu-id="a6888-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="a6888-122">Não é possível alterar a **objectCategory** de qualquer instância de uma classe Category 1.</span><span class="sxs-lookup"><span data-stu-id="a6888-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="a6888-123">Não é possível tornar uma classe ou atributo de categoria 1 desativado.</span><span class="sxs-lookup"><span data-stu-id="a6888-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="a6888-124">Não é possível alterar o **lDAPDisplayName** de uma classe ou atributo de categoria 1.</span><span class="sxs-lookup"><span data-stu-id="a6888-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="a6888-125">Não é possível renomear uma classe ou atributo de categoria 1.</span><span class="sxs-lookup"><span data-stu-id="a6888-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




