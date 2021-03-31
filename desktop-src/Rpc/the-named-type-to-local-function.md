---
title: A função named_type_to_local
description: Os stubs chamam o \_ tipo nomeado \_ para \_ função local para converter dados de um tipo transmitido para o tipo que eles apresentam para o aplicativo.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005517"
---
# <a name="the-named_type_to_local-function"></a><span data-ttu-id="8827e-104">O \_ tipo nomeado \_ para \_ função local</span><span class="sxs-lookup"><span data-stu-id="8827e-104">The named\_type\_to\_local Function</span></span>

<span data-ttu-id="8827e-105">Os stubs chamam **o \_ tipo nomeado \_ para função \_ local** para converter dados de um tipo transmitido para o tipo que eles apresentam para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8827e-105">The stubs call the **named\_type\_to\_local** function to convert data from a transmitted type to the type that they present to the application.</span></span> <span data-ttu-id="8827e-106">A função é definida como:</span><span class="sxs-lookup"><span data-stu-id="8827e-106">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

<span data-ttu-id="8827e-107">O primeiro parâmetro aponta para os dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="8827e-107">The first parameter points to the transmitted data.</span></span> <span data-ttu-id="8827e-108">A função define o segundo parâmetro para apontar para os dados apresentados.</span><span class="sxs-lookup"><span data-stu-id="8827e-108">The function sets the second parameter to point to the presented data.</span></span>

<span data-ttu-id="8827e-109">O **\_ tipo nomeado \_ para função \_ local** deve gerenciar memória para o tipo apresentado.</span><span class="sxs-lookup"><span data-stu-id="8827e-109">The **named\_type\_to\_local** function must manage memory for the presented type.</span></span> <span data-ttu-id="8827e-110">A função deve alocar memória para toda a estrutura de dados iniciada no endereço indicado pelo segundo parâmetro, exceto pelo próprio parâmetro (o stub aloca memória para o nó raiz e a transmite para a função).</span><span class="sxs-lookup"><span data-stu-id="8827e-110">The function must allocate memory for the entire data structure that starts at the address indicated by the second parameter, except for the parameter itself (the stub allocates memory for the root node and passes it to the function).</span></span> <span data-ttu-id="8827e-111">O valor do segundo parâmetro não pode ser alterado durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="8827e-111">The value of the second parameter cannot change during the call.</span></span> <span data-ttu-id="8827e-112">A função pode alterar o conteúdo nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="8827e-112">The function can change the contents at that address.</span></span>

 

 




