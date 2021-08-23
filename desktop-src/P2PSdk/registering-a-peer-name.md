---
description: 'Para registrar um nome de par, um aplicativo deve fornecer as seguintes informações: endereço IP listPeer identityPeer nameIf um nome de par não é seguro, uma identidade é opcional.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Registrando um nome de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcedbe3e405e21ec9709289e8a9237179703b1b8e81f40b449479373524beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011484"
---
# <a name="registering-a-peer-name"></a>Registrando um nome de par

Para registrar um nome de par, um aplicativo deve fornecer as seguintes informações:

-   Lista de endereços IP
-   [Identidade de par](creating-a-peer-identity.md)
-   [Nome do par](peer-names.md)

Se um nome de par não for seguro, uma identidade será opcional. Se uma identidade de par for especificada como **NULL**, o PNRP (Peer Name Resolution Protocol) usará uma identidade de par padrão interna.

## <a name="registering-a-peer-name"></a>Registrando um nome de par

Depois que a lista de endereços IP, a identidade de par e o nome de par forem identificados, o aplicativo poderá registrar um nome de par chamando [**WSASetService**](pnrp-and-wsasetservice.md). Use as diretrizes nas seções a seguir deste tópico para fazer as configurações necessárias para os parâmetros **WSASetService** e a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

### <a name="configuring-wsasetservice"></a>Configurando o WSASetService

Quando um aplicativo chama [**WSASetService**](pnrp-and-wsasetservice.md), os parâmetros devem ser configurados de acordo com as especificações a seguir:

-   *essOperation* deve ter um valor de **\_ registro RNRSERVICE**.
-   *dwFlags* deve ser zero (0).
-   *lpqsRegInfo* deve apontar para uma estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que deve ser configurada usando as diretrizes na seção **Configurando WSAQUERYSET** a seguir deste tópico.

### <a name="configuring-wsaqueryset"></a>Configurando o WSAQUERYSET

A estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve ser configurada de acordo com as especificações a seguir:

-   **dwSize** deve especificar o tamanho da estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** deve apontar para o nome de par que está sendo registrado.
-   **lpBlob** deve apontar para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** deve apontar para a lista de endereços.

> [!Note]  
> Os membros restantes são descritos em [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).

 

Depois que um nome de par é registrado, as informações ficam disponíveis para a infraestrutura de mesmo nível. No entanto, há um atraso entre o tempo de registro e a propagação das informações de registro para outros nós. Durante esse tempo, outros nós talvez não consigam resolver o par registrado recentemente.

## <a name="example-of-registering-a-peer-name"></a>Exemplo de registro de um nome de par

O trecho de código a seguir mostra como registrar um nome de par fornecendo as informações corretas ao chamar [**WSASetService**](pnrp-and-wsasetservice.md) usando a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



