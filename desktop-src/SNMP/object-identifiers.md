---
title: Identificadores de objeto (SNMP)
description: Um identificador de objeto SNMP nomeia exclusivamente um objeto e identifica seu local dentro de uma estrutura de árvore de MIB (base de informações de gerenciamento).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644107"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="fd556-103">Identificadores de objeto (SNMP)</span><span class="sxs-lookup"><span data-stu-id="fd556-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="fd556-104">Um identificador de objeto SNMP nomeia exclusivamente um objeto e identifica seu local dentro de uma estrutura de árvore de MIB (base de informações de gerenciamento).</span><span class="sxs-lookup"><span data-stu-id="fd556-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="fd556-105">Os identificadores de objeto são tipos de dados de notação de sintaxe abstrata independentes de aplicativo (ASN. 1) que consistem em uma sequência de números inteiros não negativos ou subidentificadores.</span><span class="sxs-lookup"><span data-stu-id="fd556-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="fd556-106">Os identificadores de objeto devem ter um mínimo de dois subidentificadores e não devem exceder 128 subidentificadores.</span><span class="sxs-lookup"><span data-stu-id="fd556-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="fd556-107">O ambiente de programação WinSNMP usa a estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para gerenciar identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="fd556-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="fd556-108">O formato da matriz de identificador de objeto em uma estrutura **smiOID** é um subidentificador por elemento de matriz.</span><span class="sxs-lookup"><span data-stu-id="fd556-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="fd556-109">A representação de cadeia de caracteres numérica pontilhada de um identificador de objeto separa seus subidentificadores por períodos; por exemplo, "1.2.3.4.5.6".</span><span class="sxs-lookup"><span data-stu-id="fd556-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="fd556-110">Para obter mais informações, consulte [a MIB (base de informações de gerenciamento) SNMP](the-snmp-management-information-base-mib-.md) e as RFCs relevantes.</span><span class="sxs-lookup"><span data-stu-id="fd556-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




