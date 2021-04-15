---
description: Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Enumeração UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501329"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="6695e-103">Enumeração UpdateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6695e-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="6695e-104">Define o tipo de pontos de extremidade que podem ser usados para se conectar a um serviço.</span><span class="sxs-lookup"><span data-stu-id="6695e-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="6695e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6695e-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="6695e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6695e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6695e-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="6695e-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-108">Um ponto de extremidade cliente-servidor usado para se conectar ao serviço de atualização, como Windows Update, Microsoft Update e servidor WSUS em um ambiente corporativo, para encontrar informações sobre atualizações que podem ser aplicáveis ao computador.</span><span class="sxs-lookup"><span data-stu-id="6695e-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="6695e-109">O serviço de atualização retorna informações sobre atualizações que foram publicadas, revisadas ou retiradas desde a última vez que o cliente realizou uma sincronização com o servidor.</span><span class="sxs-lookup"><span data-stu-id="6695e-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="6695e-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-111">Um ponto de extremidade de relatório que é usado quando o cliente relata os resultados de verificações, downloads e instalações de volta para o serviço de atualização.</span><span class="sxs-lookup"><span data-stu-id="6695e-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="6695e-112">No caso de serviços públicos (Windows Update e Microsoft Update), isso é feito para fins de monitoramento de qualidade.</span><span class="sxs-lookup"><span data-stu-id="6695e-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="6695e-113">No caso de serviços privados, como um servidor WSUS corporativo, o thhis tipo de ponto de extremidade também permite que o servidor colete inventário e outras informações sobre os computadores cliente sob gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="6695e-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="6695e-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-115">Um ponto de extremidade de autoatualização que é usado quando o computador cliente entra em contato com um serviço de atualização para ver se há uma nova versão do software cliente do agente de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="6695e-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="6695e-116">O ponto de extremidade de autoatualização usa um protocolo diferente do ponto de extremidade Client-Server para que as autoatualizações possam ser distribuídas mesmo se houver uma condição de erro que possa estar impedindo que a sincronização normal do cliente-servidor funcione em um computador cliente específico.</span><span class="sxs-lookup"><span data-stu-id="6695e-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="6695e-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-118">Um ponto de extremidade de regulamentação que é usado quando o computador cliente entra em contato com o serviço regulamento para agir em uma atualização específica aplicável ao computador de destino.</span><span class="sxs-lookup"><span data-stu-id="6695e-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="6695e-119">O serviço regulamento pode indicar se a atualização é "regulamentada" (também conhecida como "limitada") – em outras palavras, o serviço de regulamentação pode informar ao computador cliente que ele não deve atuar em uma atualização específica, embora essa atualização pareça ser aplicável.</span><span class="sxs-lookup"><span data-stu-id="6695e-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="6695e-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-121">Um ponto de extremidade de direcionamento simples que é usado somente com serviços privados (servidores WSUS em ambientes corporativos).</span><span class="sxs-lookup"><span data-stu-id="6695e-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="6695e-122">Em um ambiente corporativo, os computadores cliente podem ser atribuídos a grupos de destino específicos e as atualizações podem ser aprovadas para instalação em computadores em alguns grupos, mas não em outros.</span><span class="sxs-lookup"><span data-stu-id="6695e-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="6695e-123">Por exemplo, o administrador do WSUS pode criar um grupo de "teste" para computadores que são usados para testar novas atualizações, e o administrador pode aprovar atualizações lançadas recentemente para instalação em computadores no grupo de teste sem aprová-los para instalação em outros computadores da organização.</span><span class="sxs-lookup"><span data-stu-id="6695e-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="6695e-124">A troca de direcionamento simples é usada para permitir que um computador cliente se registre no servidor do WSUS e para permitir que o servidor informe ao computador cliente em qual grupo ele está.</span><span class="sxs-lookup"><span data-stu-id="6695e-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span><span class="sxs-lookup"><span data-stu-id="6695e-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-126">Um ponto de extremidade de cliente/servidor protegido que permite que um cliente obtenha informações sobre aplicativos que precisam de licenciamento para que eles possam ser usados em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6695e-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="6695e-127">Atualmente, essa estrutura de licenciamento é usada apenas pelo Windows 8 para implantar aplicativos e atualizações que são obtidas por meio da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6695e-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="6695e-128">O ponto de extremidade do servidor de cliente protegido não é usado atualmente por Windows Update, Microsoft Update ou WSUS.</span><span class="sxs-lookup"><span data-stu-id="6695e-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="6695e-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span><span class="sxs-lookup"><span data-stu-id="6695e-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="6695e-130">O ponto de extremidade de autenticação de serviço secundário é usado por um cliente para fornecer autenticação antes de obter informações sobre aplicativos que precisam de licenciamento para que eles possam ser usados em um computador cliente.</span><span class="sxs-lookup"><span data-stu-id="6695e-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="6695e-131">Atualmente, essa estrutura de licenciamento é utilizada apenas pelo Windows 8 para implantar aplicativos e atualizações que são obtidas por meio da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6695e-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="6695e-132">O ponto de extremidade de autenticação de serviço secundário não é usado atualmente por Windows Update, Microsoft Update ou WSUS.</span><span class="sxs-lookup"><span data-stu-id="6695e-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6695e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6695e-133">Requirements</span></span>



| <span data-ttu-id="6695e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6695e-134">Requirement</span></span> | <span data-ttu-id="6695e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6695e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6695e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6695e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6695e-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6695e-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="6695e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6695e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6695e-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6695e-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6695e-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6695e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6695e-141"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="6695e-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="6695e-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="6695e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6695e-143"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6695e-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




