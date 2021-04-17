---
description: Solução de segurança da família Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Solução de segurança da família Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749723"
---
# <a name="windows-family-safety-solution"></a><span data-ttu-id="8b4b8-103">Solução de segurança da família Windows</span><span class="sxs-lookup"><span data-stu-id="8b4b8-103">Windows Family Safety Solution</span></span>

<span data-ttu-id="8b4b8-104">Os principais requisitos definidos pela Microsoft para uma solução mais abrangente são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-104">Key requirements defined by Microsoft for a more comprehensive solution are as follows.</span></span> <span data-ttu-id="8b4b8-105">Observe que a definição para online é basicamente uma tecnologia voltada para a Internet, ao contrário de um cliente offline, que geralmente é associado ao computador.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-105">Note the definition for online is a primarily Internet-facing technology, unlike an offline client which is usually bounded at the computer.</span></span>

-   <span data-ttu-id="8b4b8-106">Forneça uma área única e fácil de localizar na interface do usuário do sistema operacional, em que todas as políticas de controles dos pais, controle de monitoramento de atividades e dados de atividade de uma identidade podem ser prontamente descobertas.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-106">Provide a single, easy to find area in the operating system user interface where all parental controls policies, control of activity monitoring, and activity data for an identity may be readily discovered.</span></span>

-   <span data-ttu-id="8b4b8-107">Dá suporte ao monitoramento de atividade suficiente do usuário controlado para que um pai ou guardião tenha a confiança razoável de que atividades arriscadas podem ser descobertas.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-107">Support monitoring of sufficient activity of the controlled user so that a parent or guardian has reasonable confidence that risky activities may be discovered.</span></span> <span data-ttu-id="8b4b8-108">Além disso, a reconfiguração de log das políticas do usuário controlado para que as alterações involuntárias ou não autorizadas sejam detectáveis.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-108">Also, log reconfiguration of the controlled user's policies so that unintended or unauthorized changes are discoverable.</span></span>

-   <span data-ttu-id="8b4b8-109">Expor recursos de monitoramento de atividade por meio de interfaces padrão de log de eventos do Windows Vista e forneça uma solução de visualizador na caixa.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-109">Expose activity monitoring capabilities through standard Windows Vista event logging interfaces, and provide an in-box viewer solution.</span></span> <span data-ttu-id="8b4b8-110">Defina eventos de atividade padrão e forneça a extensibilidade para a geração de eventos personalizados por ISVs.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-110">Define standard activity events, and provide for extensibility to custom event generation by ISVs.</span></span>

-   <span data-ttu-id="8b4b8-111">Promova que todo o monitoramento e as restrições de um usuário sejam ativados apenas em uma base de aceitação por pais ou tutores.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-111">Promote that all monitoring and restrictions for a user are turned on only on an opt-in basis by parents or guardians.</span></span> <span data-ttu-id="8b4b8-112">Sempre que possível, a funcionalidade de restrições deve estar completamente inativa para usuários não controlados para minimizar os riscos de segurança e compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-112">Wherever possible, restrictions functionality should be completely inactive for non-controlled users to minimize security and application compatibility risks.</span></span>

-   <span data-ttu-id="8b4b8-113">A Microsoft deve se esforçar, sempre que possível, não fazer julgamentos de valor por idade ou outros parâmetros para o usuário controlado (terceiros podem optar por fazer isso).</span><span class="sxs-lookup"><span data-stu-id="8b4b8-113">Microsoft shall strive, whenever possible, not to make value judgments by age or other parameters for the controlled user (third parties may choose to do so).</span></span> <span data-ttu-id="8b4b8-114">Essas decisões são deixadas para o pai ou o guardião, geralmente influenciadas por comunidades ou organizações.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-114">Such decisions are left up to the parent or guardian, often influenced by communities or organizations.</span></span>

-   <span data-ttu-id="8b4b8-115">Forneça implementações no produto para monitoramento de atividade offline e restrições em que algumas ou nenhuma oferta está disponível atualmente, em que a funcionalidade de risco de segurança associada está disponível no produto ou em que uma solução da Microsoft fornece funcionalidades compatíveis e robustas totalmente integradas ao design do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-115">Provide implementations in the product for offline activity monitoring and restrictions where few or no offerings are available today, where the associated safety-risk functionality is available in the product, or where a Microsoft solution provides capable and robust functionality fully integrated with the design of the operating system.</span></span>

-   <span data-ttu-id="8b4b8-116">Em geral, promova os aplicativos que executam seu próprio registro em log e restrições para melhor experiência de contexto e interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-116">Generally, promote that applications perform their own logging and restrictions for best context and UI experience.</span></span>

    <span data-ttu-id="8b4b8-117">Exceção: forneça monitoramento e restrições de atividades online abrangentes em áreas selecionadas em que o benefício para os consumidores e o setor superar os custos.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-117">Exception: Provide comprehensive online activity monitoring and restrictions in selected areas where the benefit to consumers and industry outweigh the costs.</span></span>

-   <span data-ttu-id="8b4b8-118">Exponha as configurações de interface do usuário de controles e definições de eventos de atividade usando APIs públicas para que terceiros possam consultar o estado, modificar configurações e ler logs de atividades se estiverem executando com privilégios de conta do Windows suficientes.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-118">Expose parental controls user interface settings and activity event definitions by using public APIs so that third parties may query for state, modify settings, and read activity logs if they are running with sufficient Windows account privileges.</span></span>

<span data-ttu-id="8b4b8-119">Uma meta abrangente é promover a coexistência de soluções de controles pais de terceiros com a funcionalidade interna e dar suporte à agregação de valor por meio da integração com, extensão ou fornecimento de recursos alternativos quando adequado.</span><span class="sxs-lookup"><span data-stu-id="8b4b8-119">An overarching goal is to promote third-party parental controls solutions' coexistence with the in-box functionality, and support adding value by integrating with, extending, or providing alternative capabilities where suitable.</span></span>

 

 



