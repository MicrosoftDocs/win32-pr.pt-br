---
title: Enumerações (infraestrutura de mesmo nível)
description: Usando enumerações, você pode obter uma lista de todas as entidades pares específicas que correspondem aos seus critérios.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783255"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="01313-103">Enumerações (infraestrutura de mesmo nível)</span><span class="sxs-lookup"><span data-stu-id="01313-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="01313-104">Usando enumerações, você pode obter uma lista de todas as entidades pares específicas que correspondem aos seus critérios.</span><span class="sxs-lookup"><span data-stu-id="01313-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="01313-105">**Para obter uma enumeração e recuperar os resultados**</span><span class="sxs-lookup"><span data-stu-id="01313-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="01313-106">Obtenha um identificador para a enumeração.</span><span class="sxs-lookup"><span data-stu-id="01313-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="01313-107">Chame uma função **PeerEnum** , por exemplo, chame a função de gráfico de pares de [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) .</span><span class="sxs-lookup"><span data-stu-id="01313-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="01313-108">As funções **PeerEnum** criam a enumeração e retornam um identificador para essa enumeração para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="01313-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="01313-109">Esse identificador deve ser usado para recuperar os resultados.</span><span class="sxs-lookup"><span data-stu-id="01313-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="01313-110">Opcionalmente, obtenha o número de entidades na enumeração.</span><span class="sxs-lookup"><span data-stu-id="01313-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="01313-111">Chame uma função **GetItemCount** , por exemplo, chame [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) ou [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span><span class="sxs-lookup"><span data-stu-id="01313-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="01313-112">Você pode usar o valor retornado pela função **GetItemCount** para determinar o número de itens disponíveis a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="01313-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="01313-113">Recuperar um grupo de resultados.</span><span class="sxs-lookup"><span data-stu-id="01313-113">Retrieve a group of results.</span></span> <span data-ttu-id="01313-114">Chame uma função **GetNextItem** , por exemplo, chame [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span><span class="sxs-lookup"><span data-stu-id="01313-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="01313-115">Quando um aplicativo chama uma função **GetNextItem** , ele especifica o número de entidades a serem retornadas e, em seguida, a função retorna um ponteiro para uma matriz de ponteiros para as entidades e o número de entidades, que é sempre menor ou igual ao número especificado.</span><span class="sxs-lookup"><span data-stu-id="01313-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="01313-116">Um aplicativo pode precisar chamar essa função muitas vezes — até que o número de entidades retornadas seja menor que o número solicitado.</span><span class="sxs-lookup"><span data-stu-id="01313-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="01313-117">Depois que os dados não forem necessários, libere o ponteiro para os dados.</span><span class="sxs-lookup"><span data-stu-id="01313-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="01313-118">Chame uma função **FreeData** , por exemplo, chame [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="01313-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="01313-119">Para obter mais informações, consulte [liberando dados de pares](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="01313-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="01313-120">Depois que o aplicativo não precisar do identificador para a enumeração, libere-o.</span><span class="sxs-lookup"><span data-stu-id="01313-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="01313-121">Chame uma função **Endenumeration** , por exemplo, chame [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) ou [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span><span class="sxs-lookup"><span data-stu-id="01313-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="01313-122">Exemplo de uma enumeração</span><span class="sxs-lookup"><span data-stu-id="01313-122">Example of an Enumeration</span></span>

<span data-ttu-id="01313-123">O trecho de código a seguir mostra como enumerar por meio de identidades disponíveis.</span><span class="sxs-lookup"><span data-stu-id="01313-123">The following code snippet shows you how to enumerate through available identities.</span></span>


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



