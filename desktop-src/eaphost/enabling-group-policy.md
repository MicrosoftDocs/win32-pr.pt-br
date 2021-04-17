---
title: Habilitando Política de Grupo
description: Saiba como configurar o suplicante habilitando a política de grupo. Consulte Considerações para suplicantes e exibir recursos adicionais disponíveis.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366732"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="31981-104">Habilitando Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="31981-104">Enabling Group Policy</span></span>

<span data-ttu-id="31981-105">Este tópico explica como configurar o suplicante habilitando a política de grupo.</span><span class="sxs-lookup"><span data-stu-id="31981-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="31981-106">Os suplicantes do EAPHost podem participar da diretiva de grupo para permitir que um administrador de rede configure centralmente seus computadores de rede.</span><span class="sxs-lookup"><span data-stu-id="31981-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="31981-107">O método preciso e o mecanismo pelo qual o suplicante escolhe participar na diretiva de grupo é a critério do suplicante.</span><span class="sxs-lookup"><span data-stu-id="31981-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="31981-108">Exemplos de mecanismos para participação na diretiva de grupo incluem extensões do lado do cliente/servidor, modelo administrativo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="31981-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="31981-109">Considerações ao habilitar Política de Grupo</span><span class="sxs-lookup"><span data-stu-id="31981-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="31981-110">Essas são as considerações para suplicantes em relação à diretiva de grupo e ao EAP.</span><span class="sxs-lookup"><span data-stu-id="31981-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="31981-111">A configuração de EAP sempre deve ser armazenada como XML sempre que possível e não no formato binário.</span><span class="sxs-lookup"><span data-stu-id="31981-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="31981-112">A política de grupo pode ser aplicada a qualquer computador no domínio, e a configuração do método EAP e os dados do usuário não têm garantia de serem portáteis entre as arquiteturas de processador de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="31981-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="31981-113">O XML resolve os problemas de limite da arquitetura do processador, pois o suplicante converte localmente o XML independente da arquitetura do processador na representação binária da configuração no momento da autenticação.</span><span class="sxs-lookup"><span data-stu-id="31981-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="31981-114">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="31981-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="31981-115">Perguntas frequentes gerais</span><span class="sxs-lookup"><span data-stu-id="31981-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="31981-116">[Perguntas frequentes sobre o método EAP](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="31981-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="31981-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="31981-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="31981-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="31981-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="31981-119">Se uma extensão do lado do servidor da diretiva de grupo for usada, a extensão chamará [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar os métodos disponíveis e gerar a configuração de EAP apropriada para essa política.</span><span class="sxs-lookup"><span data-stu-id="31981-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="31981-120">Em seguida, a política é enviada para os clientes de rede apropriados onde a política é aplicada.</span><span class="sxs-lookup"><span data-stu-id="31981-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31981-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31981-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31981-122">Configurando a interface do usuário do método EAP</span><span class="sxs-lookup"><span data-stu-id="31981-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="31981-123">Implementando o suporte do In-Band NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="31981-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="31981-124">Implementando o suporte a NAP para métodos EAP</span><span class="sxs-lookup"><span data-stu-id="31981-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="31981-125">Transferindo dados entre os métodos suplicante e EAP</span><span class="sxs-lookup"><span data-stu-id="31981-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="31981-126">Suplicantes do EAPHost</span><span class="sxs-lookup"><span data-stu-id="31981-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




