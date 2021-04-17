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
# <a name="required-firewall-exceptions-for-teredo"></a>Exceções de firewall necessárias para Teredo

Para que um aplicativo receba tráfego Teredo, o aplicativo deve ter permissão para receber tráfego IPv6 no firewall do host e o aplicativo é necessário para definir a opção de soquete [ \_ \_ nível de proteção IPv6](/windows/desktop/WinSock/ipv6-protection-level) como ' \_ nível de proteção \_ irrestrito '. Para habilitar esse tipo de cenário, as exceções de firewall detalhadas neste documento devem ser implementadas.

As seguintes configurações de firewall são necessárias para garantir a interoperação suave entre um firewall e o Teredo:

-   O Firewall do cliente deve permitir a resolução de teredo.ipv6.microsoft.com.
-   A porta UDP 3544 deve estar aberta para garantir que os clientes Teredo possam se comunicar com êxito com o servidor Teredo.
-   O firewall deve recuperar as portas UDP dinâmicas usadas pelo serviço Teredo no computador local chamando a função [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) ; as portas relevantes são do tipo \_ FWPM \_ porta do sistema \_ TEREDO. A função **FwpmSystemPortsGet0** deve ser implementada no lugar das funções [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) ou [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) substituídas agora.
-   O firewall permite que o sistema envie e receba pacotes UDP/IPv4 para a porta UDP 1900 na sub-rede local, pois isso permite que o tráfego de descoberta UPnP flua e tenha o potencial de melhorar as taxas de conectividade.
    > [!Note]  
    > Se essa condição não for atendida, o potencial de cenários para encontrar problemas de compatibilidade envolvendo a comunicação entre determinados tipos de NAT será introduzido; especificamente entre NATs simétricas e NATs restritos. Embora os NATs simétricos sejam populares em hotspots e NATs restritos sejam populares em residências, a comunicação entre os dois tem o potencial de falha no lado do NAT restrito.

     

-   As exceções "solicitação de eco" e "resposta de eco" ICMPv6 de entrada e saída devem ser habilitadas. Essas exceções são necessárias para garantir que um cliente Teredo possa atuar como uma retransmissão específica do host Teredo. Uma retransmissão específica do host Teredo pode ser identificada pelo endereço IPv6 nativo adicional ou um endereço 6to4 fornecido com o endereço Teredo.

Os firewalls do cliente devem dar suporte às seguintes mensagens de erro ICMPv6 e funções de descoberta por RFC 4443:



| Código    | Descrição                                    |
|---------|------------------------------------------------|
| 135/136 | Solicitação e anúncio de vizinho ICMPV6 |
| 133/134 | Solicitação e anúncio de roteador          |
| 128/129 | Solicitação e resposta de eco ICMPV6                  |
| 1       | Destino Inacessível                        |
| 2       | Pacote muito grande                               |
| 3       | Tempo excedido                                  |
| 4       | Parâmetro inválido                              |



 

Se essas mensagens não puderem ser especificamente permitidas, a isenção de todas as mensagens ICMPv6 deve ser habilitada no firewall. Além disso, o Firewall do host pode notar que os pacotes classificados por códigos 135/136 ou 133/134 são originados de, ou são direcionados para o serviço de modo de usuário **iphlpsvc** e não da pilha. Esses pacotes não devem ser descartados pelo firewall do host. O serviço Teredo é implementado principalmente no serviço auxiliar de IP do ' modo de usuário '.

Usando a API do firewall do Windows [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) para enumerar todas as regras com o sinalizador de percurso de borda definido, todos os aplicativos que desejam escutar o tráfego não solicitado são enumerados para a exceção de firewall. Informações específicas sobre o uso da opção de percurso de borda são detalhadas no [recebimento de tráfego não solicitado por Teredo](receiving-unsolicited-traffic-over-teredo.md).

Os retornos de chamada não estão associados ao seguinte código de enumeração de exemplo; é altamente recomendável que firewalls de terceiros executem a enumeração periodicamente ou sempre que o firewall detectar um novo aplicativo tentando passar pelo firewall.


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



 

 