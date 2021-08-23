---
title: Windows Estruturas dos Serviços de Implantação
description: As estruturas a seguir são usadas com Windows Deployment Services.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4315ccd3d9540334b00f43fda6522e3eae28be2d038cfdd56fcd129e9e0aed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760246"
---
# <a name="windows-deployment-services-structures"></a>Windows Estruturas dos Serviços de Implantação

As estruturas a seguir são usadas com Windows Deployment Services.



| Estrutura                                                                         | Descrição                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**ENDEREÇO \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | Especifica o endereço de rede de um pacote.                                                                        |
| [**MENSAGEM \_ DHCP PXE \_**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | Essa estrutura é usada com a API do servidor PXE Windows Deployment Services.                                        |
| [**PXE \_ DHCP \_ OPTION**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | Essa estrutura é usada com a API do servidor PXE Windows Deployment Services.                                        |
| [**PROVEDOR \_ PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | Descreve um provedor.                                                                                              |
| [**CRED da CLI do WDS \_ \_**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | Contém credenciais usadas para autorizar uma sessão de cliente.                                                           |
| [**SOLICITAÇÃO \_ TRANSPORTCLIENT do WDS \_**](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | Usado pela [**função WdsTransportClientStartSession.**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)                     |
| [**TRANSPORTCLIENT \_ SESSION \_ INFO**](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | Usado pela função de retorno [*de \_ chamada PFN WdsTransportClientSessionStartEx.*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) |
| [**WDS \_ TRANSPORTPROVIDER \_ INIT \_ PARAMS**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | Usado pela [**função de retorno de chamada WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |
| [**CONFIGURAÇÕES DO WDS \_ \_ TRANSPORTPROVIDER**](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | Usado pela [**função de retorno de chamada WdsTransportProviderInitialize.**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)            |



 

O seguinte está disponível a partir do Windows 8 e Windows Server 2012.

| Estrutura                                          | Descrição                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [**PXE \_ DHCPV6 \_ OPTION**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | Usado com a API do servidor PXE Windows Deployment Services. |
| [**PXE \_ DHCPV6 \_ MESSAGE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | Uma mensagem DHCPV6.                                         |



 

 

 




