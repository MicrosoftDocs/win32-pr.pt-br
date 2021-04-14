---
title: Gerenciando identificadores de objeto
description: A API WinSNMP fornece várias funções de utilitário WinSNMP que simplificam a manipulação de identificadores de objeto para aplicativos WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9745cb8018b6833a1ef0569e69f201c621aa38e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453696"
---
# <a name="managing-object-identifiers"></a><span data-ttu-id="c5966-103">Gerenciando identificadores de objeto</span><span class="sxs-lookup"><span data-stu-id="c5966-103">Managing Object Identifiers</span></span>

<span data-ttu-id="c5966-104">A API WinSNMP fornece várias [funções de utilitário WinSNMP](winsnmp-functions.md) que simplificam a manipulação de identificadores de objeto para aplicativos WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="c5966-104">The WinSNMP API provides several [WinSNMP utility functions](winsnmp-functions.md) that simplify the manipulation of object identifiers for WinSNMP applications.</span></span>

<span data-ttu-id="c5966-105">A função [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) converte a representação binária interna de um identificador de objeto em seu formato de cadeia de caracteres numérica pontilhada.</span><span class="sxs-lookup"><span data-stu-id="c5966-105">The [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) function converts the internal binary representation of an object identifier to its dotted numeric string format.</span></span> <span data-ttu-id="c5966-106">Ao chamar [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), especifique um buffer de cadeia de caracteres de comprimento MAXOBJIDSTRSIZE (1408 bytes) para garantir que o buffer de saída seja grande o suficiente para manter a cadeia de caracteres convertida.</span><span class="sxs-lookup"><span data-stu-id="c5966-106">When you call [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), specify a string buffer of MAXOBJIDSTRSIZE length (1408 bytes) to ensure that the output buffer is large enough to hold the converted string.</span></span> <span data-ttu-id="c5966-107">Para converter um identificador de objeto do formato de cadeia de caracteres numérica pontilhada em sua representação binária interna, chame a função [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .</span><span class="sxs-lookup"><span data-stu-id="c5966-107">To convert an object identifier from the dotted numeric string format to its internal binary representation, call the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) function.</span></span>

<span data-ttu-id="c5966-108">Para copiar um identificador de objeto SNMP, chame a função [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="c5966-108">To copy an SNMP object identifier call the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) function.</span></span> <span data-ttu-id="c5966-109">Essa função aloca qualquer memória necessária para o novo identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="c5966-109">This function allocates any necessary memory for the new object identifier.</span></span>

<span data-ttu-id="c5966-110">Um aplicativo WinSNMP deve chamar a função [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) para liberar recursos alocados para o membro **PTR** da estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) especificada pelas funções [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) e [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .</span><span class="sxs-lookup"><span data-stu-id="c5966-110">A WinSNMP application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to free resources allocated for the **ptr** member of the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure specified by both the [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) and the [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) functions.</span></span>

<span data-ttu-id="c5966-111">A função [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compara dois identificadores de objeto SNMP.</span><span class="sxs-lookup"><span data-stu-id="c5966-111">The [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) function compares two SNMP object identifiers.</span></span> <span data-ttu-id="c5966-112">O aplicativo WinSNMP pode especificar o número de subidentificadores para comparar.</span><span class="sxs-lookup"><span data-stu-id="c5966-112">The WinSNMP application can specify the number of subidentifiers to compare.</span></span> <span data-ttu-id="c5966-113">Chame **SnmpOidCompare** para determinar se dois identificadores de objeto têm prefixos comuns.</span><span class="sxs-lookup"><span data-stu-id="c5966-113">Call **SnmpOidCompare** to determine whether two object identifiers have common prefixes.</span></span>

<span data-ttu-id="c5966-114">Para obter informações adicionais sobre como gerenciar a memória alocada para identificadores de objeto, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c5966-114">For additional information about managing the memory allocated for object identifiers, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




