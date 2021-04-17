---
title: Esquema de Active Directory (esquema do AD)
description: O esquema do Microsoft Active Directory contém definições formais de cada classe de objeto que podem ser criadas em uma floresta Active Directory.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Esquema do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105811217"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="e08f0-104">Esquema de Active Directory (esquema do AD)</span><span class="sxs-lookup"><span data-stu-id="e08f0-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="e08f0-105">O esquema do Microsoft Active Directory contém definições formais de cada classe de objeto que podem ser criadas em uma floresta Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e08f0-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="e08f0-106">O esquema também contém definições formais de cada atributo que podem existir em um objeto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e08f0-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="e08f0-107">Esta seção fornece a referência para cada objeto de esquema e fornece uma breve explicação dos atributos, classes e outros objetos que compõem o esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e08f0-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="e08f0-108">A documentação a seguir contém a referência de programação para Active Directory esquema.</span><span class="sxs-lookup"><span data-stu-id="e08f0-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="e08f0-109">Se você for um usuário final tentando depurar um erro de impressora, tente pesquisar no [site da Comunidade da Microsoft](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="e08f0-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="e08f0-110">Se você for um desenvolvedor procurando uma visão geral do esquema de Active Directory, consulte os tópicos Visão geral do [esquema de Active Directory](/windows/desktop/AD/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="e08f0-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="e08f0-111">Se você estiver procurando diretrizes de programação para atualizar ou modificar o esquema, para obter mais informações sobre como estender e personalizar o esquema, consulte [estendendo o esquema](/windows/desktop/AD/extending-the-schema), bem como muitos dos tópicos nos guias de programação [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) e [Serviços AD LDS](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) .</span><span class="sxs-lookup"><span data-stu-id="e08f0-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="e08f0-112">Em cada um dos tópicos de referência, há uma seção para cada sistema operacional ao qual o tópico se aplica.</span><span class="sxs-lookup"><span data-stu-id="e08f0-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="e08f0-113">Atualmente, há suporte para os seguintes sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="e08f0-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="e08f0-114">Plataforma</span><span class="sxs-lookup"><span data-stu-id="e08f0-114">Platform</span></span>                                                      | <span data-ttu-id="e08f0-115">Nome no tópico</span><span class="sxs-lookup"><span data-stu-id="e08f0-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="e08f0-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e08f0-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="e08f0-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e08f0-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="e08f0-118">Modo de aplicativo do Microsoft Active Directory (ADAM)</span><span class="sxs-lookup"><span data-stu-id="e08f0-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="e08f0-119">ADAM</span><span class="sxs-lookup"><span data-stu-id="e08f0-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="e08f0-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e08f0-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="e08f0-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e08f0-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="e08f0-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e08f0-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="e08f0-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e08f0-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="e08f0-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e08f0-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="e08f0-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e08f0-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="e08f0-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e08f0-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="e08f0-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e08f0-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="e08f0-128">Se um sistema operacional não estiver listado no tópico, o tópico não terá suporte nesse sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="e08f0-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="e08f0-129">Por exemplo, se um tópico lista apenas o Windows Server 2003 e o ADAM, o tópico não se aplica ao Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="e08f0-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="e08f0-130">As seções a seguir contêm informações detalhadas sobre os elementos do esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e08f0-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="e08f0-131">Terminologia de esquema de Active Directory</span><span class="sxs-lookup"><span data-stu-id="e08f0-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="e08f0-132">Classes</span><span class="sxs-lookup"><span data-stu-id="e08f0-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="e08f0-133">Atributos</span><span class="sxs-lookup"><span data-stu-id="e08f0-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="e08f0-134">Sintaxes</span><span class="sxs-lookup"><span data-stu-id="e08f0-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="e08f0-135">Controlar direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="e08f0-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="e08f0-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="e08f0-136">RootDSE</span></span>](rootdse.md)

 

