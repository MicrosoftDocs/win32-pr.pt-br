---
description: A função GetAdaptersInfo preenche um ponteiro para uma \_ estrutura de \_ informações do adaptador IP com informações sobre os adaptadores de rede associados ao sistema.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gerenciando adaptadores de rede usando o GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011374"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="50559-103">Gerenciando adaptadores de rede usando o GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="50559-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="50559-104">A função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) preenche um ponteiro para uma estrutura de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) com informações sobre os adaptadores de rede associados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="50559-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="50559-105">**Para usar o GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="50559-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="50559-106">Declare um ponteiro para uma variável de [**\_ \_ informações do adaptador IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) chamada *pAdapterInfo* e uma variável **ULONG** chamada *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="50559-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="50559-107">Essas variáveis são passadas como parâmetros para a função [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="50559-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="50559-108">Além disso, crie uma variável **DWORD** chamada *dwRetVal* (para verificação de erro).</span><span class="sxs-lookup"><span data-stu-id="50559-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="50559-109">Aloque memória para as estruturas.</span><span class="sxs-lookup"><span data-stu-id="50559-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="50559-110">Faça uma chamada inicial para [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) para obter o tamanho necessário na variável *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="50559-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="50559-111">Essa chamada para a função é destinada a falhar e é usada para garantir que a variável *ulOutBufLen* especifique um tamanho suficiente para manter todas as informações retornadas para *pAdapterInfo*.</span><span class="sxs-lookup"><span data-stu-id="50559-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="50559-112">Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.</span><span class="sxs-lookup"><span data-stu-id="50559-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="50559-113">Faça uma segunda chamada para [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passando *pAdapterInfo* e *ulOutBufLen* como parâmetros e verificando o erro geral.</span><span class="sxs-lookup"><span data-stu-id="50559-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="50559-114">Retorne seu valor para a variável **DWORD** *dwRetVal* (para verificação de erro mais abrangente).</span><span class="sxs-lookup"><span data-stu-id="50559-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="50559-115">Se a chamada foi bem-sucedida, acesse alguns dos dados na estrutura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="50559-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  <span data-ttu-id="50559-116">Libere qualquer memória alocada para a estrutura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="50559-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="50559-117">Próxima etapa: [Gerenciando interfaces usando o GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="50559-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="50559-118">Etapa anterior: [recuperando informações usando GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="50559-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



