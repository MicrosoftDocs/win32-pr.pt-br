---
description: Registrando e ativando componentes em partições
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrando e ativando componentes em partições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500920"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="0b1a7-103">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="0b1a7-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="0b1a7-104">Depois que uma partição tiver sido criada, a próxima etapa será registrar os componentes COM+ dentro dessa partição.</span><span class="sxs-lookup"><span data-stu-id="0b1a7-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="0b1a7-105">Um componente é registrado em uma partição quando um novo aplicativo COM+ é criado ou quando um aplicativo COM+ existente é instalado na partição.</span><span class="sxs-lookup"><span data-stu-id="0b1a7-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="0b1a7-106">Para facilitar a administração do registro quando várias partições contêm os mesmos componentes COM+, o serviço de partições permite que um administrador Copie aplicativos ou componentes de uma partição para outra.</span><span class="sxs-lookup"><span data-stu-id="0b1a7-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="0b1a7-107">Quando um aplicativo COM+ ou um componente é copiado, todas as propriedades de partição associadas são copiadas com ele, exceto a identidade do aplicativo ou qualquer um dos membros de uma função.</span><span class="sxs-lookup"><span data-stu-id="0b1a7-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="0b1a7-108">Quando o programa cliente chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) para criar uma instância de um objeto, o com+ executa duas etapas distintas, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0b1a7-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="0b1a7-109">Localiza a partição na qual o componente reside</span><span class="sxs-lookup"><span data-stu-id="0b1a7-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="0b1a7-110">Localiza o componente correto dentro dessa partição</span><span class="sxs-lookup"><span data-stu-id="0b1a7-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="0b1a7-111">Os tópicos a seguir nesta seção descrevem essas etapas em detalhes:</span><span class="sxs-lookup"><span data-stu-id="0b1a7-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="0b1a7-112">Localizando partições durante a ativação</span><span class="sxs-lookup"><span data-stu-id="0b1a7-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="0b1a7-113">Localizando um componente para ativação</span><span class="sxs-lookup"><span data-stu-id="0b1a7-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="0b1a7-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b1a7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b1a7-115">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="0b1a7-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="0b1a7-116">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="0b1a7-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="0b1a7-117">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="0b1a7-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="0b1a7-118">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="0b1a7-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
