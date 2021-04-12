---
title: Identidade de ponto de extremidade
description: Os tipos definidos nesta seção são usados para definir a identidade de segurança de um endereço de ponto de extremidade.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Serviços Web de identidade do ponto de extremidade para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363693"
---
# <a name="endpoint-identity"></a><span data-ttu-id="0b426-106">Identidade de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="0b426-106">Endpoint Identity</span></span>

<span data-ttu-id="0b426-107">Os tipos definidos nesta seção são usados para definir a identidade de segurança de um endereço de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0b426-107">The types defined in this section are used to define the security identity of an endpoint address.</span></span>

<span data-ttu-id="0b426-108">Os seguintes elementos de API fazem parte do recuo do ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="0b426-108">The following API elements are part of endpoint indentity:</span></span>



| <span data-ttu-id="0b426-109">Enumeração</span><span class="sxs-lookup"><span data-stu-id="0b426-109">Enumeration</span></span>                                                       | <span data-ttu-id="0b426-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b426-110">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b426-111">**tipo de identidade do ponto de \_ extremidade WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-111">**WS\_ENDPOINT\_IDENTITY\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | <span data-ttu-id="0b426-112">O tipo da identidade do ponto de extremidade, usado como um seletor de subtipos de [**\_ \_ identidade do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span><span class="sxs-lookup"><span data-stu-id="0b426-112">The type of the endpoint identity, used as a selector for subtypes of [**WS\_ENDPOINT\_IDENTITY**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity).</span></span> |



 



| <span data-ttu-id="0b426-113">Estrutura</span><span class="sxs-lookup"><span data-stu-id="0b426-113">Structure</span></span>                                                               | <span data-ttu-id="0b426-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b426-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b426-115">**\_identidade do \_ ponto de extremidade WS CERT \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-115">**WS\_CERT\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | <span data-ttu-id="0b426-116">O tipo de identidade do ponto de extremidade do certificado.</span><span class="sxs-lookup"><span data-stu-id="0b426-116">The type for certificate endpoint identity .</span></span>                                                 |
| [<span data-ttu-id="0b426-117">**\_identidade do \_ ponto de extremidade do DNS do WS \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-117">**WS\_DNS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | <span data-ttu-id="0b426-118">O tipo para especificar uma identidade de ponto de extremidade representada por um nome DNS.</span><span class="sxs-lookup"><span data-stu-id="0b426-118">The type for specifying an endpoint identity represented by a DNS name.</span></span>                      |
| [<span data-ttu-id="0b426-119">**\_identidade do ponto de extremidade WS \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-119">**WS\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | <span data-ttu-id="0b426-120">O tipo base para todas as identidades do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="0b426-120">The base type for all endpoint identities.</span></span>                                                   |
| [<span data-ttu-id="0b426-121">**\_identidade de \_ ponto de extremidade RSA WS \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-121">**WS\_RSA\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | <span data-ttu-id="0b426-122">Tipo para identidade de ponto de extremidade RSA.</span><span class="sxs-lookup"><span data-stu-id="0b426-122">Type for RSA endpoint identity.</span></span>                                                              |
| [<span data-ttu-id="0b426-123">**\_identidade do \_ ponto de extremidade WS SPN \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-123">**WS\_SPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | <span data-ttu-id="0b426-124">O tipo para especificar uma identidade de ponto de extremidade representada por um SPN (nome da entidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="0b426-124">The type for specifying an endpoint identity represented by an SPN (service principal name).</span></span> |
| [<span data-ttu-id="0b426-125">**\_identidade de \_ ponto de extremidade desconhecido WS \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-125">**WS\_UNKNOWN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | <span data-ttu-id="0b426-126">O tipo de uma identidade de ponto de extremidade desconhecida.</span><span class="sxs-lookup"><span data-stu-id="0b426-126">The type for an unknown endpoint identity.</span></span>                                                   |
| [<span data-ttu-id="0b426-127">**\_identidade do \_ ponto de extremidade UPN do WS \_**</span><span class="sxs-lookup"><span data-stu-id="0b426-127">**WS\_UPN\_ENDPOINT\_IDENTITY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | <span data-ttu-id="0b426-128">O tipo para especificar uma identidade de ponto de extremidade representada por um UPN (nome principal do usuário).</span><span class="sxs-lookup"><span data-stu-id="0b426-128">The type for specifying an endpoint identity represented by a UPN (user principal name).</span></span>     |



 

 

 




