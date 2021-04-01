---
title: Descrição de segurança
description: Uma descrição de segurança é representada por uma \_ \_ estrutura de descrição de segurança do WS, e uma instância de descrições de segurança é fornecida quando você chama a função WsCreateChannel para criar um canal seguro ou a função WsCreateListener para criar um ouvinte.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Serviços Web de descrição de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104091863"
---
# <a name="security-description"></a><span data-ttu-id="2b25d-106">Descrição de segurança</span><span class="sxs-lookup"><span data-stu-id="2b25d-106">Security Description</span></span>

<span data-ttu-id="2b25d-107">Uma descrição de segurança é representada por uma estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , e uma instância de descrições de segurança é fornecida quando você chama a função [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para criar um canal seguro ou a função [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para criar um ouvinte.</span><span class="sxs-lookup"><span data-stu-id="2b25d-107">A security desciption is represented by a [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure, and an instance of a security description is supplied when you call the [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) function to create a secure channel or the [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) function to create a listener.</span></span>


## <a name="structure-of-a-security-description"></a><span data-ttu-id="2b25d-108">Estrutura de uma descrição de segurança</span><span class="sxs-lookup"><span data-stu-id="2b25d-108">Structure of a Security Description</span></span>

<span data-ttu-id="2b25d-109">O modelo básico de segurança de canal é que um canal é protegido com um ou mais tokens de segurança.</span><span class="sxs-lookup"><span data-stu-id="2b25d-109">The basic model of channel security is that a channel is secured with one or more security tokens.</span></span> <span data-ttu-id="2b25d-110">Refletindo esse modelo, a estrutura de [**\_ \_ Descrição do WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contém uma lista de associações de segurança, representadas por estruturas de [**\_ \_ Associação de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , e cada associação de segurança descreve como um token de segurança é obtido e usado no canal.</span><span class="sxs-lookup"><span data-stu-id="2b25d-110">Reflecting this model, the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure contains a list of security bindings, represented by [**WS\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) structures, and each security binding describes how one security token is obtained and used on the channel.</span></span> <span data-ttu-id="2b25d-111">O tipo de segurança usado em um canal é decidido pela seleção de subtipos de associação de segurança que são incluídos na descrição de segurança.</span><span class="sxs-lookup"><span data-stu-id="2b25d-111">The kind of security used on a channel is decided by the selection of security binding subtypes that are included in the security description.</span></span>

<span data-ttu-id="2b25d-112">Configurações de segurança opcionais específicas para uma associação de segurança são especificadas como [configurações de associação de segurança](security-binding-settings.md) na estrutura de associação de segurança; no entanto, as configurações de todo o canal independentemente das associações de segurança são especificadas diretamente como [configurações de canal de segurança](security-channel-settings.md) no campo **Propriedades** da própria descrição de segurança.</span><span class="sxs-lookup"><span data-stu-id="2b25d-112">Optional security settings that are specific to a security binding are specified as [security binding settings](security-binding-settings.md) in the security binding structure; however, channel-wide settings independent of security bindings are directly specified as [security channel settings](security-channel-settings.md) in the **properties** field of the security description itself.</span></span>

![Diagrama mostrando a estrutura de uma descrição de segurança.](images/securitydescription.png)

<span data-ttu-id="2b25d-114">Os seguintes elementos de API são usados com descrições de segurança.</span><span class="sxs-lookup"><span data-stu-id="2b25d-114">The following API elements are used with security descriptions.</span></span>

| <span data-ttu-id="2b25d-115">Estrutura</span><span class="sxs-lookup"><span data-stu-id="2b25d-115">Structure</span></span>                                                    | <span data-ttu-id="2b25d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b25d-116">Description</span></span>                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b25d-117">**\_Descrição da segurança do WS \_**</span><span class="sxs-lookup"><span data-stu-id="2b25d-117">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | <span data-ttu-id="2b25d-118">A estrutura de nível superior usada para especificar os requisitos de segurança para um canal (no lado do cliente) ou um ouvinte (no lado do servidor).</span><span class="sxs-lookup"><span data-stu-id="2b25d-118">The top-level structure used to specify the security requirements for a channel (on the client side) or a listener (on the server side).</span></span> |



 

 

 




