---
title: Estruturas SNMP
description: A tabela a seguir lista as estruturas que são usadas com SNMP.
ms.assetid: b6dacc85-893d-4825-93df-729333b491b3
keywords:
- SNMP de estruturas SNMP
- Estruturas SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254dfebeb3d468add8871d4b6f28f268341e9ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366588"
---
# <a name="snmp-structures"></a><span data-ttu-id="ab555-105">Estruturas SNMP</span><span class="sxs-lookup"><span data-stu-id="ab555-105">SNMP Structures</span></span>

<span data-ttu-id="ab555-106">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ab555-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ab555-107">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ab555-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ab555-108">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="ab555-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="ab555-109">A tabela a seguir lista as estruturas que são usadas com SNMP.</span><span class="sxs-lookup"><span data-stu-id="ab555-109">The following table lists structures that are used with SNMP.</span></span>



| <span data-ttu-id="ab555-110">Estrutura SNMP</span><span class="sxs-lookup"><span data-stu-id="ab555-110">SNMP Structure</span></span>                                         | <span data-ttu-id="ab555-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab555-111">Description</span></span>                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab555-112">**AsnAny**</span><span class="sxs-lookup"><span data-stu-id="ab555-112">**AsnAny**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnany)                           | <span data-ttu-id="ab555-113">Descreve o tipo e o valor de uma variável SNMP especificada.</span><span class="sxs-lookup"><span data-stu-id="ab555-113">Describes the type and value of a specified SNMP variable.</span></span>                                              |
| <span data-ttu-id="ab555-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab555-114">[**AsnCounter64**](/previous-versions/windows/desktop/legacy/aa377953(v=vs.85))</span></span>               | <span data-ttu-id="ab555-115">Contém um contador de 64 bits que é especificado por dois valores que descrevem seus bits de ordem inferior e de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="ab555-115">Contains a 64-bit counter that is specified by two values describing its low-order and high-order bits.</span></span> |
| [<span data-ttu-id="ab555-116">**AsnObjectIdentifier**</span><span class="sxs-lookup"><span data-stu-id="ab555-116">**AsnObjectIdentifier**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) | <span data-ttu-id="ab555-117">Descreve um OID (identificador de objeto).</span><span class="sxs-lookup"><span data-stu-id="ab555-117">Describes an object identifier (OID).</span></span>                                                                   |
| [<span data-ttu-id="ab555-118">**AsnOctetString**</span><span class="sxs-lookup"><span data-stu-id="ab555-118">**AsnOctetString**</span></span>](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring)           | <span data-ttu-id="ab555-119">Representa uma cadeia de caracteres de octetos, geralmente em valores de bytes.</span><span class="sxs-lookup"><span data-stu-id="ab555-119">Represents a string of octets, usually in byte values.</span></span>                                                  |
| [<span data-ttu-id="ab555-120">**SnmpVarBind**</span><span class="sxs-lookup"><span data-stu-id="ab555-120">**SnmpVarBind**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind)                 | <span data-ttu-id="ab555-121">Descreve uma associação de variável SNMP.</span><span class="sxs-lookup"><span data-stu-id="ab555-121">Describes an SNMP variable binding.</span></span>                                                                     |
| [<span data-ttu-id="ab555-122">**SnmpVarBindList**</span><span class="sxs-lookup"><span data-stu-id="ab555-122">**SnmpVarBindList**</span></span>](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist)         | <span data-ttu-id="ab555-123">Contém uma lista de associações de variáveis SNMP.</span><span class="sxs-lookup"><span data-stu-id="ab555-123">Contains a list of SNMP variable bindings.</span></span>                                                              |



 

 

 