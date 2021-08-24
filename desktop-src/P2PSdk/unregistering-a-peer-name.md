---
description: Quando você cancela o registro de um nome de par, um nome registrado é removido de uma nuvem PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Cancelando o registro de um nome de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675006"
---
# <a name="unregistering-a-peer-name"></a>Cancelando o registro de um nome de par

Quando você cancela o registro de um nome de par, um nome registrado é removido de uma nuvem PNRP (Peer Name Resolution Protocol).

## <a name="unregistering-a-peer-name"></a>Cancelando o registro de um nome de par

Para cancelar o registro de um nome de par, chame [**WSASetService**](pnrp-and-wsasetservice.md). O parâmetro *essOperation* deve ter um valor de **RNRSERVICE \_ delete**. Use as diretrizes nas seções a seguir deste tópico para fazer as configurações necessárias para os parâmetros **WSASetService** e a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

## <a name="configuring-wsasetservice"></a>Configurando o WSASetService

Quando um aplicativo chama [**WSASetService**](pnrp-and-wsasetservice.md), os parâmetros devem ser configurados de acordo com as especificações a seguir:

-   *essOperation* deve ter um valor de **RNRSERVICE \_ delete**.
-   *dwFlags* deve ser zero (0).
-   *lpqsRegInfo* deve apontar para uma estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , que deve ser configurada usando as diretrizes na seção a seguir deste tópico.

## <a name="configuring-wsaqueryset"></a>Configurando o WSAQUERYSET

A estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) deve ser configurada de acordo com as especificações a seguir:

-   **dwSize** deve especificar o tamanho da estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** deve apontar para o nome de par que está sendo cancelado.
-   **lpBlob** deve apontar para uma estrutura [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** deve apontar para a lista de endereços.

> [!Note]  
> Os membros restantes são descritos em [**PNRP e WSASetService**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Um exemplo de cancelamento do registro de um nome de par

O trecho de código a seguir mostra como cancelar o registro de um nome de par fornecendo as informações corretas ao chamar [**WSASetService**](pnrp-and-wsasetservice.md) usando a estrutura [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



