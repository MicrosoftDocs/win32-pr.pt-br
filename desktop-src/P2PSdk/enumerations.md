---
title: Enumerações (infraestrutura de mesmo nível)
description: Usando enumerações, você pode obter uma lista de todas as entidades pares específicas que correspondem aos seus critérios.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514866001734fb0ba0d73c94d5d4d8f8b4cfc6987d121f058a6bfcb00f792c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887626"
---
# <a name="enumerations-peer-infrastructure"></a>Enumerações (infraestrutura de mesmo nível)

Usando enumerações, você pode obter uma lista de todas as entidades pares específicas que correspondem aos seus critérios.

**Para obter uma enumeração e recuperar os resultados**

1.  Obtenha um identificador para a enumeração. Chame uma função **PeerEnum** , por exemplo, chame a função de gráfico de pares de [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) . As funções **PeerEnum** criam a enumeração e retornam um identificador para essa enumeração para o aplicativo de chamada. Esse identificador deve ser usado para recuperar os resultados.
2.  Opcionalmente, obtenha o número de entidades na enumeração. Chame uma função **GetItemCount** , por exemplo, chame [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) ou [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).
    > [!Note]  
    > Você pode usar o valor retornado pela função **GetItemCount** para determinar o número de itens disponíveis a serem recuperados.

     

3.  Recuperar um grupo de resultados. Chame uma função **GetNextItem** , por exemplo, chame [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Quando um aplicativo chama uma função **GetNextItem** , ele especifica o número de entidades a serem retornadas e, em seguida, a função retorna um ponteiro para uma matriz de ponteiros para as entidades e o número de entidades, que é sempre menor ou igual ao número especificado. Um aplicativo pode precisar chamar essa função muitas vezes — até que o número de entidades retornadas seja menor que o número solicitado.

     

4.  Depois que os dados não forem necessários, libere o ponteiro para os dados. Chame uma função **FreeData** , por exemplo, chame [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) ou [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).
    > [!Note]  
    > Para obter mais informações, consulte [liberando dados de pares](freeing-peer-data.md).

     

5.  Depois que o aplicativo não precisar do identificador para a enumeração, libere-o. Chame uma função **Endenumeration** , por exemplo, chame [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) ou [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Exemplo de uma enumeração

O trecho de código a seguir mostra como enumerar por meio de identidades disponíveis.


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



 

 



