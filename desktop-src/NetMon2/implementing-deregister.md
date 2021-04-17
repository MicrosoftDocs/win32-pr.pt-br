---
description: Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função de cancelamento de registro para todos os protocolos que ele identifica. Cada DLL do analisador deve implementar uma função de cancelamento de registro para cada protocolo compatível com a DLL do analisador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementando cancelamento de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747939"
---
# <a name="implementing-deregister"></a><span data-ttu-id="03e81-104">Implementando cancelamento de registro</span><span class="sxs-lookup"><span data-stu-id="03e81-104">Implementing Deregister</span></span>

<span data-ttu-id="03e81-105">Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função de [**cancelamento de registro**](deregister.md) para todos os protocolos que ele identifica.</span><span class="sxs-lookup"><span data-stu-id="03e81-105">Network Monitor passes all the frames of a capture to the parsers, and then starts calling the [**Deregister**](deregister.md) function for all the protocols it identifies.</span></span> <span data-ttu-id="03e81-106">Cada DLL do analisador deve implementar uma função de **cancelamento de registro** para cada protocolo compatível com a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="03e81-106">Each parser DLL must implement a **Deregister** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="03e81-107">Cada implementação da função de [**cancelamento de registro**](deregister.md) deve chamar a função [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar os recursos que são usados para criar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="03e81-107">Each implementation of the [**Deregister**](deregister.md) function must call the [**DestroyProtocolDatabase**](destroypropertydatabase.md) function to release the resources that are used to create the database.</span></span>

<span data-ttu-id="03e81-108">O procedimento a seguir identifica a única etapa necessária para implementar o [**cancelamento de registro**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="03e81-108">The following procedure identifies the one step necessary to implement [**Deregister**](deregister.md).</span></span>

<span data-ttu-id="03e81-109">**Para implementar o cancelamento de registro para um protocolo**</span><span class="sxs-lookup"><span data-stu-id="03e81-109">**To implement Deregister for one protocol**</span></span>

-   <span data-ttu-id="03e81-110">Chame [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar os recursos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="03e81-110">Call [**DestroyProtocolDatabase**](destroypropertydatabase.md) to release the database resources.</span></span>

<span data-ttu-id="03e81-111">A seguir está uma implementação básica do [**cancelamento do registro**](deregister.md).</span><span class="sxs-lookup"><span data-stu-id="03e81-111">The following is a basic implementation of [**Deregister**](deregister.md).</span></span> <span data-ttu-id="03e81-112">Observe que o exemplo de código mostra a versão dos recursos que são usados para criar um banco de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="03e81-112">Note that the code example shows the release of resources that are used to create a property database.</span></span>

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



