---
title: Objetos de identificador de recurso
description: A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636755"
---
# <a name="resource-handle-objects"></a><span data-ttu-id="90f43-104">Objetos de identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="90f43-104">Resource Handle Objects</span></span>

<span data-ttu-id="90f43-105">A estrutura de um objeto de recurso é restrita à implementação do Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="90f43-105">The structure of a resource object is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="90f43-106">Um aplicativo WinSNMP pode acessar um objeto de recurso com um identificador.</span><span class="sxs-lookup"><span data-stu-id="90f43-106">A WinSNMP application can access a resource object with a handle.</span></span>

<span data-ttu-id="90f43-107">A implementação pode alocar um dos seguintes tipos de identificadores de recursos para um aplicativo WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="90f43-107">The implementation can allocate one of the following types of resource handles for a WinSNMP application.</span></span>

| <span data-ttu-id="90f43-108">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="90f43-108">Handle type</span></span>        | <span data-ttu-id="90f43-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="90f43-109">Description</span></span>                       |
|--------------------|-----------------------------------|
| <span data-ttu-id="90f43-110">**\_sessão HSNMP**</span><span class="sxs-lookup"><span data-stu-id="90f43-110">**HSNMP\_SESSION**</span></span> | <span data-ttu-id="90f43-111">Tratar de uma sessão WinSNMP</span><span class="sxs-lookup"><span data-stu-id="90f43-111">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="90f43-112">**\_entidade HSNMP**</span><span class="sxs-lookup"><span data-stu-id="90f43-112">**HSNMP\_ENTITY**</span></span>  | <span data-ttu-id="90f43-113">Identificador para uma entidade SNMP</span><span class="sxs-lookup"><span data-stu-id="90f43-113">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="90f43-114">**contexto de HSNMP \_**</span><span class="sxs-lookup"><span data-stu-id="90f43-114">**HSNMP\_CONTEXT**</span></span> | <span data-ttu-id="90f43-115">Tratar de um contexto WinSNMP</span><span class="sxs-lookup"><span data-stu-id="90f43-115">Handle to a WinSNMP context</span></span>       |
| <span data-ttu-id="90f43-116">**PDU de HSNMP \_**</span><span class="sxs-lookup"><span data-stu-id="90f43-116">**HSNMP\_PDU**</span></span>     | <span data-ttu-id="90f43-117">Identificador para uma unidade de dados de protocolo</span><span class="sxs-lookup"><span data-stu-id="90f43-117">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="90f43-118">**HSNMP \_ VBL**</span><span class="sxs-lookup"><span data-stu-id="90f43-118">**HSNMP\_VBL**</span></span>     | <span data-ttu-id="90f43-119">Identificador para uma lista de associação de variável</span><span class="sxs-lookup"><span data-stu-id="90f43-119">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="90f43-120">Um aplicativo WinSNMP pode solicitar que a implementação crie ou exclua identificadores de recurso, mas a implementação executa a operação.</span><span class="sxs-lookup"><span data-stu-id="90f43-120">A WinSNMP application can request that the implementation create or delete resource handles, but the implementation performs the operation.</span></span> <span data-ttu-id="90f43-121">Para obter informações adicionais sobre como liberar recursos individuais, consulte as funções [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)e [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .</span><span class="sxs-lookup"><span data-stu-id="90f43-121">For additional information about freeing individual resources, see the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), and [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) functions.</span></span>

 

 




