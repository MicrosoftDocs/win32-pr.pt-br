---
title: Exceções de firewall necessárias para Teredo
description: Para que um aplicativo receba tráfego Teredo, o aplicativo deve ter permissão para receber tráfego IPv6 no firewall do host e o aplicativo é necessário para definir a opção de soquete \_ nível de proteção IPv6 \_ como ' \_ nível de proteção \_ irrestrito '.
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbc2fcf0f7c8b1f5fe51afc056dc8c8ff7c7916a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761944"
---
# <a name="required-firewall-exceptions-for-teredo"></a><span data-ttu-id="7f71f-103">Exceções de firewall necessárias para Teredo</span><span class="sxs-lookup"><span data-stu-id="7f71f-103">Required Firewall Exceptions for Teredo</span></span>

<span data-ttu-id="7f71f-104">Para que um aplicativo receba tráfego Teredo, o aplicativo deve ter permissão para receber tráfego IPv6 no firewall do host e o aplicativo é necessário para definir a opção de soquete [ \_ \_ nível de proteção IPv6](/windows/desktop/WinSock/ipv6-protection-level) como ' \_ nível de proteção \_ irrestrito '.</span><span class="sxs-lookup"><span data-stu-id="7f71f-104">For an application to receive Teredo traffic, the application must be permitted to receive IPv6 traffic in the host firewall, and the application is required to set the socket option [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) to 'PROTECTION\_LEVEL\_UNRESTRICTED'.</span></span> <span data-ttu-id="7f71f-105">Para habilitar esse tipo de cenário, as exceções de firewall detalhadas neste documento devem ser implementadas.</span><span class="sxs-lookup"><span data-stu-id="7f71f-105">To enable this type of scenario, the firewall exceptions detailed in this document must be implemented.</span></span>

<span data-ttu-id="7f71f-106">As seguintes configurações de firewall são necessárias para garantir a interoperação suave entre um firewall e o Teredo:</span><span class="sxs-lookup"><span data-stu-id="7f71f-106">The following firewall configurations are required to ensure smooth interoperation between a firewall and Teredo:</span></span>

-   <span data-ttu-id="7f71f-107">O Firewall do cliente deve permitir a resolução de teredo.ipv6.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="7f71f-107">The client firewall must allow resolution of teredo.ipv6.microsoft.com.</span></span>
-   <span data-ttu-id="7f71f-108">A porta UDP 3544 deve estar aberta para garantir que os clientes Teredo possam se comunicar com êxito com o servidor Teredo.</span><span class="sxs-lookup"><span data-stu-id="7f71f-108">UDP Port 3544 must be open to ensure that Teredo clients can successfully communicate with the Teredo server.</span></span>
-   <span data-ttu-id="7f71f-109">O firewall deve recuperar as portas UDP dinâmicas usadas pelo serviço Teredo no computador local chamando a função [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) ; as portas relevantes são do tipo \_ FWPM \_ porta do sistema \_ TEREDO.</span><span class="sxs-lookup"><span data-stu-id="7f71f-109">The firewall must retrieve dynamic UDP ports used by Teredo service on the local machine by calling the [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) function; relevant ports are of type FWPM\_SYSTEM\_PORT\_TEREDO.</span></span> <span data-ttu-id="7f71f-110">A função **FwpmSystemPortsGet0** deve ser implementada no lugar das funções [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) ou [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) substituídas agora.</span><span class="sxs-lookup"><span data-stu-id="7f71f-110">The **FwpmSystemPortsGet0** function should be implemented in place of the now deprecated [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) or [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) functions.</span></span>
-   <span data-ttu-id="7f71f-111">O firewall permite que o sistema envie e receba pacotes UDP/IPv4 para a porta UDP 1900 na sub-rede local, pois isso permite que o tráfego de descoberta UPnP flua e tenha o potencial de melhorar as taxas de conectividade.</span><span class="sxs-lookup"><span data-stu-id="7f71f-111">The firewall permits the system to send and receive UDP/IPv4 packets to UDP port 1900 on the local subnet as this allows UPnP discovery traffic to flow and has the potential to improve connectivity rates.</span></span>
    > [!Note]  
    > <span data-ttu-id="7f71f-112">Se essa condição não for atendida, o potencial de cenários para encontrar problemas de compatibilidade envolvendo a comunicação entre determinados tipos de NAT será introduzido; especificamente entre NATs simétricas e NATs restritos.</span><span class="sxs-lookup"><span data-stu-id="7f71f-112">If this condition is not met, the potential for scenarios to encounter compatibility issues involving communication between certain NAT types is introduced; specifically between Symmetric NATs and Restricted NATs.</span></span> <span data-ttu-id="7f71f-113">Embora os NATs simétricos sejam populares em hotspots e NATs restritos sejam populares em residências, a comunicação entre os dois tem o potencial de falha no lado do NAT restrito.</span><span class="sxs-lookup"><span data-stu-id="7f71f-113">While Symmetric NATs are popular in hotspots and Restricted NATs are popular in homes, communication between the two has the potential to fault on the side of the Restricted NAT.</span></span>

     

-   <span data-ttu-id="7f71f-114">As exceções "solicitação de eco" e "resposta de eco" ICMPv6 de entrada e saída devem ser habilitadas.</span><span class="sxs-lookup"><span data-stu-id="7f71f-114">Incoming and outgoing ICMPv6 "Echo Request" and "Echo Reply" exceptions must be enabled.</span></span> <span data-ttu-id="7f71f-115">Essas exceções são necessárias para garantir que um cliente Teredo possa atuar como uma retransmissão específica do host Teredo.</span><span class="sxs-lookup"><span data-stu-id="7f71f-115">These exceptions are necessary to ensure that a Teredo client can act as a Teredo host-specific relay.</span></span> <span data-ttu-id="7f71f-116">Uma retransmissão específica do host Teredo pode ser identificada pelo endereço IPv6 nativo adicional ou um endereço 6to4 fornecido com o endereço Teredo.</span><span class="sxs-lookup"><span data-stu-id="7f71f-116">A Teredo host-specific relay can be identified by the additional native IPv6 address or a 6to4 address supplied with the Teredo address.</span></span>

<span data-ttu-id="7f71f-117">Os firewalls do cliente devem dar suporte às seguintes mensagens de erro ICMPv6 e funções de descoberta por RFC 4443:</span><span class="sxs-lookup"><span data-stu-id="7f71f-117">Client firewalls must support the following ICMPv6 error messages and discovery functions per RFC 4443:</span></span>



| <span data-ttu-id="7f71f-118">Código</span><span class="sxs-lookup"><span data-stu-id="7f71f-118">Code</span></span>    | <span data-ttu-id="7f71f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f71f-119">Description</span></span>                                    |
|---------|------------------------------------------------|
| <span data-ttu-id="7f71f-120">135/136</span><span class="sxs-lookup"><span data-stu-id="7f71f-120">135/136</span></span> | <span data-ttu-id="7f71f-121">Solicitação e anúncio de vizinho ICMPV6</span><span class="sxs-lookup"><span data-stu-id="7f71f-121">ICMPV6 Neighbor Solicitation and Advertisement</span></span> |
| <span data-ttu-id="7f71f-122">133/134</span><span class="sxs-lookup"><span data-stu-id="7f71f-122">133/134</span></span> | <span data-ttu-id="7f71f-123">Solicitação e anúncio de roteador</span><span class="sxs-lookup"><span data-stu-id="7f71f-123">Router Solicitation and Advertisement</span></span>          |
| <span data-ttu-id="7f71f-124">128/129</span><span class="sxs-lookup"><span data-stu-id="7f71f-124">128/129</span></span> | <span data-ttu-id="7f71f-125">Solicitação e resposta de eco ICMPV6</span><span class="sxs-lookup"><span data-stu-id="7f71f-125">ICMPV6 Echo Request and Reply</span></span>                  |
| <span data-ttu-id="7f71f-126">1</span><span class="sxs-lookup"><span data-stu-id="7f71f-126">1</span></span>       | <span data-ttu-id="7f71f-127">Destino Inacessível</span><span class="sxs-lookup"><span data-stu-id="7f71f-127">Destination Unreachable</span></span>                        |
| <span data-ttu-id="7f71f-128">2</span><span class="sxs-lookup"><span data-stu-id="7f71f-128">2</span></span>       | <span data-ttu-id="7f71f-129">Pacote muito grande</span><span class="sxs-lookup"><span data-stu-id="7f71f-129">Packet Too Large</span></span>                               |
| <span data-ttu-id="7f71f-130">3</span><span class="sxs-lookup"><span data-stu-id="7f71f-130">3</span></span>       | <span data-ttu-id="7f71f-131">Tempo excedido</span><span class="sxs-lookup"><span data-stu-id="7f71f-131">Time Exceeded</span></span>                                  |
| <span data-ttu-id="7f71f-132">4</span><span class="sxs-lookup"><span data-stu-id="7f71f-132">4</span></span>       | <span data-ttu-id="7f71f-133">Parâmetro inválido</span><span class="sxs-lookup"><span data-stu-id="7f71f-133">Invalid Parameter</span></span>                              |



 

<span data-ttu-id="7f71f-134">Se essas mensagens não puderem ser especificamente permitidas, a isenção de todas as mensagens ICMPv6 deve ser habilitada no firewall.</span><span class="sxs-lookup"><span data-stu-id="7f71f-134">If these messages cannot be specifically allowed, then the exemption of all ICMPv6 messages should be enabled on the firewall.</span></span> <span data-ttu-id="7f71f-135">Além disso, o Firewall do host pode notar que os pacotes classificados por códigos 135/136 ou 133/134 são originados de, ou são direcionados para o serviço de modo de usuário **iphlpsvc** e não da pilha.</span><span class="sxs-lookup"><span data-stu-id="7f71f-135">Additionally, the host firewall may notice that the packets classified by codes 135/136 or 133/134 originate from, or are targeted to, the user mode service **iphlpsvc** and not from the stack.</span></span> <span data-ttu-id="7f71f-136">Esses pacotes não devem ser descartados pelo firewall do host.</span><span class="sxs-lookup"><span data-stu-id="7f71f-136">These packets must not be dropped by the host firewall.</span></span> <span data-ttu-id="7f71f-137">O serviço Teredo é implementado principalmente no serviço auxiliar de IP do ' modo de usuário '.</span><span class="sxs-lookup"><span data-stu-id="7f71f-137">The Teredo service is implemented primarily within the 'user mode' IP Helper service.</span></span>

<span data-ttu-id="7f71f-138">Usando a API do firewall do Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) para enumerar todas as regras com o sinalizador de percurso de borda definido, todos os aplicativos que desejam escutar o tráfego não solicitado são enumerados para a exceção de firewall.</span><span class="sxs-lookup"><span data-stu-id="7f71f-138">Using the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows Firewall API to enumerate all rules with the Edge Traversal flag set, all applications that want to listen for unsolicited traffic are enumerated for the firewall exception.</span></span> <span data-ttu-id="7f71f-139">Informações específicas sobre o uso da opção de percurso de borda são detalhadas no [recebimento de tráfego não solicitado por Teredo](receiving-unsolicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="7f71f-139">Specific information regarding the use of the Edge Traversal option is detailed in [Receiving Unsolicited Traffic Over Teredo](receiving-unsolicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="7f71f-140">Os retornos de chamada não estão associados ao seguinte código de enumeração de exemplo; é altamente recomendável que firewalls de terceiros executem a enumeração periodicamente ou sempre que o firewall detectar um novo aplicativo tentando passar pelo firewall.</span><span class="sxs-lookup"><span data-stu-id="7f71f-140">Callbacks are not associated with the following sample enumeration code; it is strongly recommended that third party firewalls perform the enumeration periodically, or whenever the firewall detects a new application attempting to go through the firewall.</span></span>


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 