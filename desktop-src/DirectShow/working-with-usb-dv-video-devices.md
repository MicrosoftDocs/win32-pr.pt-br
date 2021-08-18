---
description: Trabalhando com dispositivos de vídeo USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Trabalhando com dispositivos de vídeo USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1f83fb490f4bd1e71714dcb0658d01a41d6e45af6f3e89436f6e32c1cdc985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071731"
---
# <a name="working-with-usb-dv-video-devices"></a>Trabalhando com dispositivos de vídeo USB DV

Este tópico descreve como escrever aplicativos para dispositivos de vídeo USB (barramento serial universal) que capturam vídeo DV.

O formato DV padrão tem uma taxa de dados de cerca de 25 megabits por segundo (Mbps). Quando o USB foi introduzido pela primeira vez, ele não tinha largura de banda suficiente para dar suporte ao vídeo DV. No entanto, o USB 2,0 pode dar suporte a até 480 Mbps, o que é mais do que suficiente para vídeo DV. A especificação da classe de dispositivo de vídeo USB (UVC), lançada em 2003, define o formato de carga para dispositivos de vídeo DV USB. um Driver de classe Windows Driver Model (WDM) para dispositivos UVC foi introduzido no Windows XP Service Pack 2.

Na maioria dos aspectos, o driver UVC dá suporte ao mesmo modelo de programação que o driver MSDV para dispositivos IEEE 1394. Os aplicativos escritos para MSDV devem exigir apenas pequenas modificações para dar suporte a dispositivos UVC.

O driver UVC se comporta de forma diferente do driver MSDV nas seguintes áreas:

-   [Modo de dispositivo](device-mode.md)
-   [Formato do fluxo](stream-format.md)
-   [Formato de sinal](signal-format.md)
-   [Pesquisa de local de fita](tape-location-search.md)
-   [Transmita DV de arquivo para fita](transmit-dv-from-file-to-tape.md).

Para determinar qual driver está sendo usado, chame [**IAMExtDevice:: get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). O driver MSDV retorna o \_ sinalizador porta de desenvolvimento \_ 1394 e o driver UVC retorna o \_ sinalizador USB da porta de desenvolvimento \_ .

**Nós de dispositivo**

Na terminologia USB, os pontos de extremidade são os pontos nos quais os dados entram ou saem do dispositivo. Um ponto de extremidade tem uma direção de fluxo de dados, uma entrada (do dispositivo para o host) ou saída (do host para o dispositivo). Isso pode ajudar a considerar essas direções como sendo relativas ao host. A entrada vai para o host; a saída é proveniente do host. O diagrama a seguir ilustra os dois pontos de extremidade.

![pontos de extremidade USB](images/ksnodes01.png)

Em um dispositivo UVC, as funções do dispositivo são divididas logicamente em componentes chamados unidades e terminais. Uma unidade recebe um ou mais fluxos de dados como entrada e entrega exatamente um fluxo como saída. Um terminal é o ponto inicial ou final de um fluxo de dados. Os pontos de extremidade USB correspondem aos terminais, mas as direções são invertidas: um ponto final de entrada é representado por um terminal de saída, e vice-versa. O diagrama a seguir mostra a relação entre terminais e pontos de extremidade.

![unidades de UVC e terminais](images/ksnodes02.png)

Além disso, nem todos os terminais correspondem a um ponto de extremidade USB. O termo ponto de extremidade refere-se especificamente a conexões USB e um dispositivo pode enviar ou receber dados por meio de conexões não USB. Por exemplo, uma câmera de vídeo é um terminal de entrada e uma tela de LCD é um terminal de saída.

No filtro de proxy KS, as unidades e os terminais são representados como nós dentro do filtro. O nó de termo é mais geral do que a unidade de termos e o terminal porque os dispositivos não USB também podem ter nós. Para obter informações sobre os nós em um filtro, consulte o filtro para a interface [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) . Os tipos de nó são identificados por GUIDs. Os nós de seletor são nós que podem alternar entre duas ou mais entradas. Nós de seletor expõem a interface [**iseleger**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .

O código a seguir testa se um PIN de saída em um filtro recebe entrada de um nó de um determinado tipo.


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



