---
description: Esta seção descreve a estrutura de QOS (qualidade de serviço) específica do protocolo para ATM, que está contida no campo ProviderSpecific da estrutura de QOS.
ms.assetid: ec7882f7-7197-439a-82a4-ff081505a9d7
title: Extensão de QoS de ATM do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075c9dcbd8b9148f41d39c99e2118ed638a577ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090349"
---
# <a name="winsock-atm-qos-extension"></a><span data-ttu-id="67341-103">Extensão de QoS de ATM do Winsock</span><span class="sxs-lookup"><span data-stu-id="67341-103">Winsock ATM QoS Extension</span></span>

<span data-ttu-id="67341-104">Esta seção descreve a estrutura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos)(qualidade de serviço) específica do protocolo para ATM, que está contida no campo [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) da estrutura de **QoS** .</span><span class="sxs-lookup"><span data-stu-id="67341-104">This section describes the protocol-specific Quality of Service ([**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)) structure for ATM, which is contained in the [ProviderSpecific](/previous-versions/aa374467(v=vs.80)) field of the **QOS** structure.</span></span> <span data-ttu-id="67341-105">Observe que o uso dessa estrutura **QoS** específica de ATM é opcional pelos clientes do Windows Sockets 2, e o provedor de serviços ATM é necessário para mapear a estrutura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) genérica para os elementos de informações de Q. 2931 apropriados.</span><span class="sxs-lookup"><span data-stu-id="67341-105">Note that the use of this ATM-specific **QOS** structure is optional by Windows Sockets 2 clients, and the ATM service provider is required to map the generic [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure to appropriate Q.2931 information elements.</span></span> <span data-ttu-id="67341-106">No entanto, se a estrutura **FLOWSPEC** genérica e a estrutura **QoS** específica do ATM forem especificadas, o valor especificado na estrutura **QoS** específica do ATM deverá ter precedência caso haja conflitos.</span><span class="sxs-lookup"><span data-stu-id="67341-106">However, if both the generic **FLOWSPEC** structure and ATM-specific **QOS** structure are specified, the value specified in the ATM-specific **QOS** structure should take precedence should there be any conflicts.</span></span> <span data-ttu-id="67341-107">Consulte a seção especificação da API do Windows Sockets 2 2,7 para obter mais informações sobre as provisões de QoS e a estrutura **FLOWSPEC** .</span><span class="sxs-lookup"><span data-stu-id="67341-107">See Windows Sockets 2 API Specification Section 2.7 for more information about QoS provisions and **FLOWSPEC** structure.</span></span>

<span data-ttu-id="67341-108">A estrutura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) específica de protocolo para ATM é uma concatenação das estruturas do elemento de informações 2931 (IE), que são definidas no texto a seguir.</span><span class="sxs-lookup"><span data-stu-id="67341-108">The protocol-specific [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) structure for ATM is a concatenation of Q.2931 information element (IE) structures, which are defined in the following text.</span></span> <span data-ttu-id="67341-109">Se um aplicativo omitir um IE que exige 3. x, o provedor de serviços deverá inserir um valor padrão razoável, colocando as informações na estrutura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) em conta, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="67341-109">If an application omits an IE that UNI 3.x mandates, the service provider should insert a reasonable default value, taking the information in the [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) structure into account if applicable.</span></span>

<span data-ttu-id="67341-110">A manipulação de s repetidas depende do próprio IE.</span><span class="sxs-lookup"><span data-stu-id="67341-110">The handling of repeated IEs is dependent on the IE itself.</span></span> <span data-ttu-id="67341-111">Se um IE for repetido e for um que pode ser repetido de acordo com a especificação UNI do fórum ATM, o provedor deverá tratá-lo corretamente.</span><span class="sxs-lookup"><span data-stu-id="67341-111">If an IE is repeated and it is one that is allowed to be repeated per the ATM Forum UNI specification then the provider must handle it properly.</span></span> <span data-ttu-id="67341-112">Nesse caso, Order na lista determina a ordem de preferência, com elementos que aparecem anteriormente na lista sendo mais preferenciais.</span><span class="sxs-lookup"><span data-stu-id="67341-112">In this case, order in the list determines preference order, with elements appearing earlier in the list being more preferred.</span></span> <span data-ttu-id="67341-113">Se um IE for repetido e isso não for permitido por uma especificação UNI do fórum ATM, o provedor poderá falhar a solicitação do cliente (a opção preferencial) ou usar o último IE desse tipo encontrado.</span><span class="sxs-lookup"><span data-stu-id="67341-113">If an IE is repeated and this is not allowed per ATM Forum UNI specification, the provider may either fail the request from the client (the preferred option) or use the last IE of that type found.</span></span>

<span data-ttu-id="67341-114">Cada estrutura individual do IE é formatada da seguinte maneira e identificada pelo campo **IEType** :</span><span class="sxs-lookup"><span data-stu-id="67341-114">Each individual IE structure is formatted in the following manner and identified by the **IEType** field:</span></span>

``` syntax
typedef struct {
    Q2931_IE_TYPE IEType;
    ULONG         IELength;
    UCHAR         IE[1];
} Q2931_IE;
```

<span data-ttu-id="67341-115">Os valores válidos para o campo **IEType** são definidos como:</span><span class="sxs-lookup"><span data-stu-id="67341-115">Legal values for the **IEType** field are defined as:</span></span>

``` syntax
typedef enum {
    IE_AALParameters,
    IE_TrafficDescriptor,
    IE_BroadbandBearerCapability,
    IE_BHLI,
    IE_BLLI,
    IE_CalledPartyNumber,
    IE_CalledPartySubaddress,
    IE_CallingPartyNumber,
    IE_CallingPartySubaddress,
    IE_Cause,
    IE_QOSClass,
    IE_TransitNetworkSelection,
} Q2931_IE_TYPE;
```

<span data-ttu-id="67341-116">O campo do **IE** é sobreposto por uma estrutura específica do IE e o campo **IELength** é o comprimento total em bytes da estrutura do IE, incluindo os campos **IEType** e **IELength** .</span><span class="sxs-lookup"><span data-stu-id="67341-116">The **IE** field is overlaid by a specific IE structure and the **IELength** field is the total length in bytes of the IE structure including the **IEType** and **IELength** fields.</span></span> <span data-ttu-id="67341-117">A semântica e os valores válidos para cada elemento dessas estruturas do IE são por especificação UNI 3. x de ATM.</span><span class="sxs-lookup"><span data-stu-id="67341-117">The semantics and legal values for each element of these IE structures are per ATM UNI 3.x specification.</span></span> <span data-ttu-id="67341-118">\_O campo SAP \_ ausente pode ser usado para esses elementos opcionais para uma determinada estrutura do IE, por especificação uni 3. x de ATM.</span><span class="sxs-lookup"><span data-stu-id="67341-118">SAP\_FIELD\_ABSENT can be used for those elements that are optional for a given IE structure, per ATM UNI 3.x specification.</span></span>

 

 
