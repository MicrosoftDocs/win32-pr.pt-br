---
title: Gerenciando uma lista de associação de variáveis
description: A função SnmpGetVb recupera informações de associação de variáveis de uma lista de associação de variáveis. A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005271"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="db7c7-104">Gerenciando uma lista de associação de variáveis</span><span class="sxs-lookup"><span data-stu-id="db7c7-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="db7c7-105">A função [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) recupera informações de associação de variáveis de uma lista de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="db7c7-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="db7c7-106">A função recupera o nome da variável e o valor associado da variável da entrada de associação de variável especificada pelo aplicativo WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="db7c7-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="db7c7-107">Para atualizar entradas de associação de variáveis em uma lista de associação de variáveis, chame a função [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) .</span><span class="sxs-lookup"><span data-stu-id="db7c7-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="db7c7-108">A função **SnmpSetVb** também acrescenta novas entradas de associação de variável a uma lista de associação de variável existente.</span><span class="sxs-lookup"><span data-stu-id="db7c7-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="db7c7-109">O aplicativo WinSNMP deve chamar a função [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) para remover entradas de uma lista de associação de variável.</span><span class="sxs-lookup"><span data-stu-id="db7c7-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="db7c7-110">Para recuperar, modificar ou excluir uma entrada de associação de variável, o aplicativo WinSNMP deve especificar a posição da entrada na lista de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="db7c7-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="db7c7-111">Uma chamada para a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associa uma lista de associação de variável a uma PDU.</span><span class="sxs-lookup"><span data-stu-id="db7c7-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="db7c7-112">Uma chamada para a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) recupera uma lista de associação de variável de uma PDU.</span><span class="sxs-lookup"><span data-stu-id="db7c7-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="db7c7-113">Uma associação de variável individual não está diretamente associada a uma PDU, mas está diretamente associada à sua inclusão em uma lista de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="db7c7-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




