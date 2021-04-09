---
title: S (APIs UPnP)
description: Contém termos relacionados a UPnP que começam com a letra S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008714"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="bd331-103">S (APIs UPnP)</span><span class="sxs-lookup"><span data-stu-id="bd331-103">S (UPnP APIs)</span></span>

<span data-ttu-id="bd331-104">Contém termos relacionados a UPnP que começam com a letra S.</span><span class="sxs-lookup"><span data-stu-id="bd331-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="bd331-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) i J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="bd331-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bd331-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**serviço**</span><span class="sxs-lookup"><span data-stu-id="bd331-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="bd331-107">Um serviço é uma unidade funcional lógica.</span><span class="sxs-lookup"><span data-stu-id="bd331-107">A service is a logical functional unit.</span></span> <span data-ttu-id="bd331-108">Os serviços expõem ações e modelam alguns ou todos os Estados de um dispositivo físico usando variáveis de estado.</span><span class="sxs-lookup"><span data-stu-id="bd331-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="bd331-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Descrição do serviço**</span><span class="sxs-lookup"><span data-stu-id="bd331-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="bd331-110">Uma descrição de serviço é uma lista das ações que um serviço fornece e as variáveis de estado associadas às ações.</span><span class="sxs-lookup"><span data-stu-id="bd331-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="bd331-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**objeto de serviço**</span><span class="sxs-lookup"><span data-stu-id="bd331-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="bd331-112">Um objeto de serviço é a representação da API do ponto de controle de um serviço.</span><span class="sxs-lookup"><span data-stu-id="bd331-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="bd331-113">Um objeto de serviço implementa a interface [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="bd331-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bd331-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**tipo de serviço**</span><span class="sxs-lookup"><span data-stu-id="bd331-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="bd331-115">Um tipo de serviço é um URN que identifica um serviço.</span><span class="sxs-lookup"><span data-stu-id="bd331-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="bd331-116">Há uma relação um-para-um entre um modelo de serviço UPnP e um tipo de serviço.</span><span class="sxs-lookup"><span data-stu-id="bd331-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="bd331-117">Vários tipos de serviço padrão são definidos pelos comitês de trabalho do fórum UPnP.</span><span class="sxs-lookup"><span data-stu-id="bd331-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="bd331-118">Os tipos de serviço estão no formato urn: schemas-UPnP-org: Service: serviceType: Version.</span><span class="sxs-lookup"><span data-stu-id="bd331-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="bd331-119">Por exemplo, um tipo de serviço do verificador poderia ser urn: schemas-UPnP-org: Service: scanner: 1.</span><span class="sxs-lookup"><span data-stu-id="bd331-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="bd331-120">Os fornecedores UPnP podem especificar serviços adicionais.</span><span class="sxs-lookup"><span data-stu-id="bd331-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="bd331-121">Esses serviços são indicados por urn: nome-do-domínio: serviço: serviceType: versão em que Domain-Name é um nome de domínio registrado para o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="bd331-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="bd331-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**variável de estado**</span><span class="sxs-lookup"><span data-stu-id="bd331-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="bd331-123">Uma variável de estado é um dado que descreve alguma parte do estado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="bd331-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




