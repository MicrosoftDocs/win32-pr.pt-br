---
title: Identificadores de objeto (AD DS)
description: Os OIDs (identificadores de objeto) são valores numéricos exclusivos emitidos por várias autoridades emissores para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "105748298"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="0f880-104">Identificadores de objeto (AD DS)</span><span class="sxs-lookup"><span data-stu-id="0f880-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="0f880-105">Os OIDs (identificadores de objeto) são valores numéricos exclusivos emitidos por várias autoridades emissores para identificar exclusivamente elementos de dados, sintaxes e outras partes de aplicativos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="0f880-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="0f880-106">Os OIDs são encontrados em aplicativos OSI, em diretórios X. 500, SNMP e em outros aplicativos onde a exclusividade é importante.</span><span class="sxs-lookup"><span data-stu-id="0f880-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="0f880-107">Os OIDs são baseados em uma estrutura de árvore, na qual uma autoridade emissora superior, como o ISO, aloca uma ramificação da árvore para uma subautoridade que, por sua vez, pode alocar subramificações.</span><span class="sxs-lookup"><span data-stu-id="0f880-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="0f880-108">O protocolo LDAP (RFC 2251) requer um serviço de diretório para identificar classes de objeto, atributos e sintaxes com OIDs.</span><span class="sxs-lookup"><span data-stu-id="0f880-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="0f880-109">Isso faz parte do herdado do LDAP X. 500.</span><span class="sxs-lookup"><span data-stu-id="0f880-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="0f880-110">Os OIDs em Active Directory Domain Services incluem alguns emitidos pelo ISO para classes e atributos X. 500 e alguns emitidos pela Microsoft e outras autoridades emissora.</span><span class="sxs-lookup"><span data-stu-id="0f880-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="0f880-111">A notação OID é uma cadeia de números pontilhada, por exemplo, "1.2.840.113556.1.5.9", que é descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f880-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="0f880-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0f880-112">Value</span></span>  | <span data-ttu-id="0f880-113">Significado</span><span class="sxs-lookup"><span data-stu-id="0f880-113">Meaning</span></span>          | <span data-ttu-id="0f880-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f880-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="0f880-115">1</span><span class="sxs-lookup"><span data-stu-id="0f880-115">1</span></span>      | <span data-ttu-id="0f880-116">ISO</span><span class="sxs-lookup"><span data-stu-id="0f880-116">ISO</span></span>              | <span data-ttu-id="0f880-117">Identifica a autoridade raiz.</span><span class="sxs-lookup"><span data-stu-id="0f880-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="0f880-118">2</span><span class="sxs-lookup"><span data-stu-id="0f880-118">2</span></span>      | <span data-ttu-id="0f880-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="0f880-119">ANSI</span></span>             | <span data-ttu-id="0f880-120">Designação de grupo atribuída pela ISO.</span><span class="sxs-lookup"><span data-stu-id="0f880-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="0f880-121">840</span><span class="sxs-lookup"><span data-stu-id="0f880-121">840</span></span>    | <span data-ttu-id="0f880-122">EUA</span><span class="sxs-lookup"><span data-stu-id="0f880-122">USA</span></span>              | <span data-ttu-id="0f880-123">Designação de país/região atribuída pelo grupo.</span><span class="sxs-lookup"><span data-stu-id="0f880-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="0f880-124">113556</span><span class="sxs-lookup"><span data-stu-id="0f880-124">113556</span></span> | <span data-ttu-id="0f880-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f880-125">Microsoft</span></span>        | <span data-ttu-id="0f880-126">Designação de organização atribuída pelo país/região.</span><span class="sxs-lookup"><span data-stu-id="0f880-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="0f880-127">1</span><span class="sxs-lookup"><span data-stu-id="0f880-127">1</span></span>      | <span data-ttu-id="0f880-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="0f880-128">Active Directory</span></span> | <span data-ttu-id="0f880-129">Atribuído pela organização.</span><span class="sxs-lookup"><span data-stu-id="0f880-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="0f880-130">5</span><span class="sxs-lookup"><span data-stu-id="0f880-130">5</span></span>      | <span data-ttu-id="0f880-131">Classes</span><span class="sxs-lookup"><span data-stu-id="0f880-131">Classes</span></span>          | <span data-ttu-id="0f880-132">Atribuído pela organização.</span><span class="sxs-lookup"><span data-stu-id="0f880-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="0f880-133">9</span><span class="sxs-lookup"><span data-stu-id="0f880-133">9</span></span>      | <span data-ttu-id="0f880-134">classe de **usuário**</span><span class="sxs-lookup"><span data-stu-id="0f880-134">**user** class</span></span>   | <span data-ttu-id="0f880-135">Atribuído pela organização.</span><span class="sxs-lookup"><span data-stu-id="0f880-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="0f880-136">Para obter mais informações e uma discussão sobre dois procedimentos usados para obter OIDs válidos para uso na extensão do esquema de Active Directory, consulte [obtendo um identificador de objeto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="0f880-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




