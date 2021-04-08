---
description: Ao usar o serviço de eventos COM+, há etapas que você pode seguir para garantir que quaisquer informações confidenciais contidas em um evento não sejam comprometidas.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considerações de segurança de eventos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920610"
---
# <a name="com-events-security-considerations"></a><span data-ttu-id="71b55-103">Considerações de segurança de eventos COM+</span><span class="sxs-lookup"><span data-stu-id="71b55-103">COM+ Events Security Considerations</span></span>

<span data-ttu-id="71b55-104">Ao usar o serviço de eventos COM+, há etapas que você pode seguir para garantir que quaisquer informações confidenciais contidas em um evento não sejam comprometidas.</span><span class="sxs-lookup"><span data-stu-id="71b55-104">When using the COM+ events service, there are steps you can take to ensure that any sensitive information contained in an event is not compromised.</span></span>

<span data-ttu-id="71b55-105">Os editores de eventos devem ter em mente que qualquer parte que possa gravar em seu catálogo COM+ pode assinar seus eventos.</span><span class="sxs-lookup"><span data-stu-id="71b55-105">Event publishers should keep in mind that any party that can write to your COM+ catalog can subscribe to your events.</span></span> <span data-ttu-id="71b55-106">Portanto, se as informações contidas em um objeto de classe de evento forem confidenciais, você deverá usar a ferramenta de administração de serviços de componentes para verificar se as comunicações com assinantes são criptografadas para o aplicativo que contém os componentes da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="71b55-106">Therefore, if the information contained in an event class object is sensitive, you should use the Component Services administration tool to verify that communications with subscribers are encrypted for the application that contains the event class components.</span></span> <span data-ttu-id="71b55-107">(Na guia **segurança** da folha de propriedades do aplicativo com+, selecione **privacidade do pacote** como o **nível de autenticação para as configurações de chamadas** .) Além disso, você deve usar [filtros de eventos](filtering-events-in-com-.md) para ajudar a garantir que os eventos sejam entregues somente aos assinantes apropriados.</span><span class="sxs-lookup"><span data-stu-id="71b55-107">(On the **Security** tab of the COM+ application property sheet, select **Packet Privacy** as the **Authentication Level for Calls** setting.) Also, you should use [event filters](filtering-events-in-com-.md) to help ensure that events are delivered only to the appropriate subscribers.</span></span>

<span data-ttu-id="71b55-108">Os assinantes de eventos devem ter em mente que uma parte mal-intencionada com acesso à sua rede e o conhecimento de seu objeto de classe de evento poderia criar eventos falsos.</span><span class="sxs-lookup"><span data-stu-id="71b55-108">Event subscribers should keep in mind that a malicious party with access to your network and knowledge of your event class object could create false events.</span></span> <span data-ttu-id="71b55-109">Portanto, você deve usar a [segurança baseada em função](role-based-security-administration.md) para ajudar a garantir que os chamadores dos métodos do seu objeto de classe de evento tenham as credenciais apropriadas para executar as ações descritas pela sua implementação.</span><span class="sxs-lookup"><span data-stu-id="71b55-109">You should therefore use [role-based security](role-based-security-administration.md) to help ensure that callers of your event class object's methods have appropriate credentials to perform the actions described by your implementation.</span></span>

<span data-ttu-id="71b55-110">Para ajudar a proteger Publicadores e assinantes, use o serviço de eventos COM+ em uma rede privada de hosts confiáveis que é isolada da Internet por um firewall.</span><span class="sxs-lookup"><span data-stu-id="71b55-110">To help protect both publishers and subscribers, use the COM+ Events service on a private network of trusted hosts that is isolated from the Internet by a firewall.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71b55-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71b55-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b55-112">Segurança do COM+</span><span class="sxs-lookup"><span data-stu-id="71b55-112">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="71b55-113">Filtrando eventos no COM+</span><span class="sxs-lookup"><span data-stu-id="71b55-113">Filtering Events in COM+</span></span>](filtering-events-in-com-.md)
</dt> <dt>

[<span data-ttu-id="71b55-114">O objeto de classe de evento COM+</span><span class="sxs-lookup"><span data-stu-id="71b55-114">The COM+ Event Class Object</span></span>](the-com--event-class-object.md)
</dt> </dl>

 

 



