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
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="b95bd-103">Estruturas de serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="b95bd-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="b95bd-104">As estruturas a seguir são usadas com os serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="b95bd-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="b95bd-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="b95bd-105">Structure</span></span>                                                                         | <span data-ttu-id="b95bd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b95bd-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b95bd-107">**\_endereço PXE**</span><span class="sxs-lookup"><span data-stu-id="b95bd-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="b95bd-108">Especifica o endereço de rede para um pacote.</span><span class="sxs-lookup"><span data-stu-id="b95bd-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="b95bd-109">**\_mensagem DHCP do PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="b95bd-110">Essa estrutura é usada com a API do servidor PXE dos serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="b95bd-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="b95bd-111">**\_opção DHCP do PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="b95bd-112">Essa estrutura é usada com a API do servidor PXE dos serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="b95bd-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="b95bd-113">**\_provedor PXE**</span><span class="sxs-lookup"><span data-stu-id="b95bd-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="b95bd-114">Descreve um provedor.</span><span class="sxs-lookup"><span data-stu-id="b95bd-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="b95bd-115">**\_credenciais da CLI do WDS \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="b95bd-116">Contém as credenciais usadas para autorizar uma sessão de cliente.</span><span class="sxs-lookup"><span data-stu-id="b95bd-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="b95bd-117">**\_solicitação de TRANSPORTCLIENT do WDS \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="b95bd-118">Usado pela função [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .</span><span class="sxs-lookup"><span data-stu-id="b95bd-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="b95bd-119">**\_informações da sessão TRANSPORTCLIENT \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="b95bd-120">Usado pela função de retorno de chamada [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) .</span><span class="sxs-lookup"><span data-stu-id="b95bd-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="b95bd-121">**parâmetros de inicialização de transporte do WDS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="b95bd-122">Usado pela função de retorno de chamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="b95bd-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="b95bd-123">**configurações de transporte do WDS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="b95bd-124">Usado pela função de retorno de chamada [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="b95bd-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="b95bd-125">A seguir está disponível a partir do Windows 8 e do Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b95bd-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="b95bd-126">Estrutura</span><span class="sxs-lookup"><span data-stu-id="b95bd-126">Structure</span></span>                                          | <span data-ttu-id="b95bd-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="b95bd-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="b95bd-128">**\_Opção de DHCPv6 PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="b95bd-129">Usado com a API do servidor PXE dos serviços de implantação do Windows.</span><span class="sxs-lookup"><span data-stu-id="b95bd-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="b95bd-130">**\_Mensagem DHCPv6 do PXE \_**</span><span class="sxs-lookup"><span data-stu-id="b95bd-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="b95bd-131">Uma mensagem DHCPV6.</span><span class="sxs-lookup"><span data-stu-id="b95bd-131">A DHCPV6 message.</span></span>                                         |



 

 

 




