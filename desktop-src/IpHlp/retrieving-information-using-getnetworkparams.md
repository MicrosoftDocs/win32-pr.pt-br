---
description: Preenche um ponteiro para uma estrutura de informações FIXAs \_ com dados sobre as configurações de rede atuais.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Recuperando informações usando GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169872"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="1f595-103">Recuperando informações usando GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="1f595-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="1f595-104">A função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) preenche um ponteiro para uma estrutura de [**\_ informações fixas**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) com dados sobre as configurações de rede atuais.</span><span class="sxs-lookup"><span data-stu-id="1f595-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="1f595-105">**Para usar o GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="1f595-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="1f595-106">Declare um ponteiro para um objeto de [**\_ informações fixo**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) chamado *PFixedInfo* e um objeto **ULONG** chamado *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="1f595-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="1f595-107">Essas variáveis são passadas como parâmetros para a função [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="1f595-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="1f595-108">Além disso, crie uma variável **DWORD** *dwRetVal* (usada para verificação de erro).</span><span class="sxs-lookup"><span data-stu-id="1f595-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="1f595-109">Aloque memória para as estruturas.</span><span class="sxs-lookup"><span data-stu-id="1f595-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="1f595-110">O tamanho de *ulOutBufLen* não é suficiente para manter as informações.</span><span class="sxs-lookup"><span data-stu-id="1f595-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="1f595-111">Consulte a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="1f595-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="1f595-112">Faça uma chamada inicial para [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) para obter o tamanho necessário para a variável *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="1f595-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="1f595-113">Essa função falhará e será usada para garantir que a variável *ulOutBufLen* especifique um tamanho suficiente para manter todos os dados retornados para *pFixedInfo*.</span><span class="sxs-lookup"><span data-stu-id="1f595-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="1f595-114">Esse é um modelo de programação comum para as estruturas de dados e funções desse tipo.</span><span class="sxs-lookup"><span data-stu-id="1f595-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="1f595-115">Faça uma segunda chamada para [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) usando a verificação de erro geral e retornando seu valor para a variável **DWORD** *dwRetVal*; usado para verificação de erros mais avançada.</span><span class="sxs-lookup"><span data-stu-id="1f595-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="1f595-116">Se a chamada foi bem-sucedida, acesse os dados da estrutura de dados *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="1f595-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  <span data-ttu-id="1f595-117">Libere qualquer memória alocada para a estrutura *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="1f595-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="1f595-118">Próxima etapa: [Gerenciando adaptadores de rede usando GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="1f595-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="1f595-119">Etapa anterior: [criando um aplicativo auxiliar de IP básico](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="1f595-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



