---
title: Estruturas de serviços de implantação do Windows
description: As estruturas a seguir são usadas com os serviços de implantação do Windows.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006016"
---
# <a name="windows-deployment-services-structures"></a>Estruturas de serviços de implantação do Windows

As estruturas a seguir são usadas com os serviços de implantação do Windows.



| Estrutura                                                                         | Descrição                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**\_endereço PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Especifica o endereço de rede para um pacote.                                                                        |
| [**\_mensagem DHCP do PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Essa estrutura é usada com a API do servidor PXE dos serviços de implantação do Windows.                                        |
| [**\_opção DHCP do PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Essa estrutura é usada com a API do servidor PXE dos serviços de implantação do Windows.                                        |
| [**\_provedor PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Descreve um provedor.                                                                                              |
| [**\_credenciais da CLI do WDS \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contém as credenciais usadas para autorizar uma sessão de cliente.                                                           |
| [**\_solicitação de TRANSPORTCLIENT do WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Usado pela função [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .                     |
| [**\_informações da sessão TRANSPORTCLIENT \_**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Usado pela função de retorno de chamada [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) . |
| [**parâmetros de inicialização de transporte do WDS \_ \_ \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Usado pela função de retorno de chamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |
| [**configurações de transporte do WDS \_ \_**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Usado pela função de retorno de chamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .            |



 

A seguir está disponível a partir do Windows 8 e do Windows Server 2012.

| Estrutura                                          | Descrição                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**\_Opção de DHCPv6 PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Usado com a API do servidor PXE dos serviços de implantação do Windows. |
| [**\_Mensagem DHCPv6 do PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Uma mensagem DHCPV6.                                         |



 

 

 




