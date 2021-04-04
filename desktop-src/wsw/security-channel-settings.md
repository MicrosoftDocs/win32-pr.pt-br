---
title: Configurações de canal de segurança
description: As configurações de canal de segurança controlam a maneira como a segurança é aplicada e verificada em um canal.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Serviços Web de configurações de canal de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085010"
---
# <a name="security-channel-settings"></a><span data-ttu-id="2505b-106">Configurações de canal de segurança</span><span class="sxs-lookup"><span data-stu-id="2505b-106">Security Channel Settings</span></span>

<span data-ttu-id="2505b-107">As configurações de canal de segurança controlam a maneira como a segurança é aplicada e verificada em um canal.</span><span class="sxs-lookup"><span data-stu-id="2505b-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="2505b-108">Cada configuração de canal de segurança é representada por uma coleção de pares de propriedade-valor, com as chaves de propriedade definidas pela [**\_ identificação de \_ propriedade \_ de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2505b-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="2505b-109">Cada propriedade na coleção tem um valor padrão razoável.</span><span class="sxs-lookup"><span data-stu-id="2505b-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="2505b-110">Devido a esses valores padrão, é possível definir e usar uma descrição de segurança sem especificar as configurações de canal de segurança.</span><span class="sxs-lookup"><span data-stu-id="2505b-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="2505b-111">[As configurações de associação de segurança](security-binding-settings.md) contêm coleções semelhantes de pares de propriedade-valor cujas chaves são definidas pela estrutura de propriedade de [**Associação de segurança do WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) .</span><span class="sxs-lookup"><span data-stu-id="2505b-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="2505b-112">A diferença entre esses dois tipos de configurações é que as configurações de canal de segurança têm como escopo uma descrição de segurança (ou seja, elas contêm propriedades de segurança de todo o canal), enquanto as configurações de associação de segurança têm como escopo uma das associações de segurança, e pode haver muitas associações de segurança.</span><span class="sxs-lookup"><span data-stu-id="2505b-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="2505b-113">Consequentemente, por exemplo, uma descrição de segurança personalizada que contenha três associações de segurança terá um recipiente de configurações de canal de segurança para todo o canal e três pacotes de configurações de ligação de segurança, um para cada associação de segurança.</span><span class="sxs-lookup"><span data-stu-id="2505b-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="2505b-114">As seguintes enumerações são usadas com as configurações de canal de segurança:</span><span class="sxs-lookup"><span data-stu-id="2505b-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="2505b-115">**\_nível de proteção do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="2505b-116">**\_ID da \_ Propriedade do token de segurança da solicitação WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="2505b-117">**\_ID do \_ algoritmo de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="2505b-118">**\_ID da \_ Propriedade do algoritmo de segurança do WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="2505b-119">**\_layout do \_ cabeçalho de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="2505b-120">**\_versão do \_ cabeçalho de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="2505b-121">**\_ID da \_ propriedade de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="2505b-122">**\_uso do \_ carimbo de data/hora do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="2505b-123">**\_ID da \_ Propriedade do token de segurança \_ \_ do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="2505b-124">As seguintes estruturas são usadas com as configurações de canal de segurança:</span><span class="sxs-lookup"><span data-stu-id="2505b-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="2505b-125">**\_propriedade de \_ token de segurança de solicitação WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="2505b-126">**\_Propriedade do \_ algoritmo de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="2505b-127">**\_conjunto de \_ algoritmos de segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="2505b-128">**\_propriedade de segurança WS \_**</span><span class="sxs-lookup"><span data-stu-id="2505b-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="2505b-129">**\_Propriedade do \_ token de segurança \_ \_ do WS XML**</span><span class="sxs-lookup"><span data-stu-id="2505b-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




