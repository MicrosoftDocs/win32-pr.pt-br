---
description: A função GetInterfaceInfo preenche um ponteiro para uma \_ estrutura de informações de interface IP \_ com informações sobre as interfaces associadas ao sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gerenciando interfaces usando o GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811024"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="ce50d-103">Gerenciando interfaces usando o GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="ce50d-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="ce50d-104">A função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) preenche um ponteiro para uma estrutura de [**\_ \_ informações de interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) com informações sobre as interfaces associadas ao sistema.</span><span class="sxs-lookup"><span data-stu-id="ce50d-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="ce50d-105">**Para usar o GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="ce50d-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="ce50d-106">Declare um ponteiro para um objeto de [**\_ \_ informações de interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) chamado `pInfo` e um objeto **ULONG** chamado `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="ce50d-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="ce50d-107">Declare também um objeto **DWORD** chamado `dwRetVal` (usado para verificação de erro).</span><span class="sxs-lookup"><span data-stu-id="ce50d-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="ce50d-108">Aloque memória para as estruturas.</span><span class="sxs-lookup"><span data-stu-id="ce50d-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="ce50d-109">O tamanho de `ulOutBufLen` não é suficiente para manter as informações.</span><span class="sxs-lookup"><span data-stu-id="ce50d-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="ce50d-110">Consulte a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="ce50d-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="ce50d-111">Faça uma chamada inicial para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) para obter o tamanho necessário na `ulOutBufLen` variável.</span><span class="sxs-lookup"><span data-stu-id="ce50d-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="ce50d-112">Essa chamada para a função é destinada a falhar e é usada para garantir que a `ulOutBufLen` variável especifique um tamanho suficiente para manter todas as informações retornadas para `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="ce50d-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="ce50d-113">Este é um modelo de programação comum no auxiliar de IP para estruturas de dados e funções desse tipo.</span><span class="sxs-lookup"><span data-stu-id="ce50d-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="ce50d-114">Faça uma segunda chamada para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) com verificação de erro geral e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais avançada).</span><span class="sxs-lookup"><span data-stu-id="ce50d-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="ce50d-115">Se a chamada foi bem-sucedida, acesse os dados da `pInfo` estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="ce50d-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="ce50d-116">O% WS na primeira linha denota uma cadeia de caracteres larga.</span><span class="sxs-lookup"><span data-stu-id="ce50d-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="ce50d-117">Isso é usado porque o atributo **Name** da estrutura [**do \_ \_ \_ mapa do índice do adaptador IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` é um **WCHAR**, que é uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ce50d-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="ce50d-118">Libere qualquer memória alocada para a estrutura *pInfo* .</span><span class="sxs-lookup"><span data-stu-id="ce50d-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="ce50d-119">Próxima etapa: [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="ce50d-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="ce50d-120">Etapa anterior: [Gerenciando adaptadores de rede usando GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ce50d-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



