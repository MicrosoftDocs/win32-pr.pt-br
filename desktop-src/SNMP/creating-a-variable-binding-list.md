---
title: Criando uma lista de associações de variáveis
description: A função SnmpCreateVbl cria uma nova lista de associação de variáveis.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e9ef7aa208e2e2f887d14c0e124f3bb659ff8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159937"
---
# <a name="creating-a-variable-binding-list"></a><span data-ttu-id="3d431-103">Criando uma lista de associações de variáveis</span><span class="sxs-lookup"><span data-stu-id="3d431-103">Creating a Variable Binding List</span></span>

<span data-ttu-id="3d431-104">A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) cria uma nova lista de associação de variáveis.</span><span class="sxs-lookup"><span data-stu-id="3d431-104">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function creates a new variable binding list.</span></span> <span data-ttu-id="3d431-105">Se o aplicativo WinSNMP especificar um nome de variável e um valor, a função criará a lista e adicionará o nome e o valor como a primeira entrada na lista.</span><span class="sxs-lookup"><span data-stu-id="3d431-105">If the WinSNMP application specifies a variable name and a value, the function creates the list and adds the name and value as the first entry in the list.</span></span> <span data-ttu-id="3d431-106">Se o aplicativo especificar **NULL** para o nome da variável, a função criará uma lista vazia.</span><span class="sxs-lookup"><span data-stu-id="3d431-106">If the application specifies **NULL** for the variable name, the function creates an empty list.</span></span>

<span data-ttu-id="3d431-107">Para copiar uma lista de associação de variável, chame a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) .</span><span class="sxs-lookup"><span data-stu-id="3d431-107">To copy a variable binding list, call the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function.</span></span> <span data-ttu-id="3d431-108">A função cria uma nova lista de associação de variáveis e inicializa a nova lista com uma cópia dos dados na lista de associações de variáveis de origem.</span><span class="sxs-lookup"><span data-stu-id="3d431-108">The function creates a new variable binding list and initializes the new list with a copy of the data in the source variable binding list.</span></span>

<span data-ttu-id="3d431-109">A função [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e a função [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) alocam qualquer memória necessária para a nova lista de associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="3d431-109">The [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) function and the [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) function allocate any necessary memory for the new variable binding list.</span></span> <span data-ttu-id="3d431-110">O aplicativo WinSNMP deve liberar os recursos associados a essas listas.</span><span class="sxs-lookup"><span data-stu-id="3d431-110">The WinSNMP application must release the resources associated with these lists.</span></span> <span data-ttu-id="3d431-111">É recomendável que o aplicativo faça isso correspondendo a cada chamada para [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) e [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) com uma chamada correspondente para a função [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) quando for apropriado liberar a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="3d431-111">It is recommended that the application do this by matching each call to [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) and [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) with a corresponding call to the [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) function when it is appropriate to free the allocated memory.</span></span>

 

 




