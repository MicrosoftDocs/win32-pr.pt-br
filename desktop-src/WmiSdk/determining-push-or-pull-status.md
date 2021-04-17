---
description: Você pode modelar um provedor de classe como um provedor de Push ou pull, que especifica como um provedor espera interagir com o WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Determinando o status de Push ou pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812080"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="93197-103">Determinando o status de Push ou pull</span><span class="sxs-lookup"><span data-stu-id="93197-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="93197-104">Você pode modelar um provedor de classe como um provedor de Push ou pull, que especifica como um provedor espera interagir com o WMI.</span><span class="sxs-lookup"><span data-stu-id="93197-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="93197-105">Os provedores de pull recebem uma solicitação do WMI e atendem à solicitação gerando os dados dinamicamente ou recuperando-os de um cache local.</span><span class="sxs-lookup"><span data-stu-id="93197-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="93197-106">Os provedores de pull também devem implementar um grande número de interfaces.</span><span class="sxs-lookup"><span data-stu-id="93197-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="93197-107">Um provedor de pull gera definições de classe dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="93197-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="93197-108">Normalmente, os dados gerenciados por um provedor de pull são alterados com frequência, exigindo que o provedor gere a classe dinamicamente ou recupere a classe de um cache local sempre que um aplicativo emitir uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="93197-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="93197-109">Um provedor de pull deve implementar seus próprios mecanismos de recuperação de dados, cache e notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="93197-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="93197-110">Como a maioria dos provedores são provedores de pull, a documentação neste arquivo pressupõe que você está criando um provedor de pull, a menos que explicitamente declarado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="93197-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="93197-111">Por outro lado, o WMI usa dados no repositório do WMI para lidar com todas as solicitações de aplicativos para provedores de envio por push.</span><span class="sxs-lookup"><span data-stu-id="93197-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="93197-112">Os provedores de push também usam menos métodos de interface e, portanto, são mais fáceis de implementar.</span><span class="sxs-lookup"><span data-stu-id="93197-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="93197-113">Um provedor de push usa o repositório WMI como uma área de armazenamento para obter informações sobre o objeto gerenciado e atualiza essas informações somente durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="93197-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="93197-114">Por exemplo, o provedor de classes WDM incluído na seção WMI do SDK (Software Development Kit) do Microsoft Windows é modelado como um provedor de push.</span><span class="sxs-lookup"><span data-stu-id="93197-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="93197-115">Usando o repositório WMI como uma área de armazenamento, um provedor de push Obtém os seguintes benefícios em um provedor de pull:</span><span class="sxs-lookup"><span data-stu-id="93197-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="93197-116">O provedor não precisa implementar um cache local para armazenar dados.</span><span class="sxs-lookup"><span data-stu-id="93197-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="93197-117">O provedor não precisa dar suporte à recuperação de dados; em vez disso, o provedor pode contar com o WMI para fornecer suporte de recuperação.</span><span class="sxs-lookup"><span data-stu-id="93197-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="93197-118">Quando um aplicativo solicita dados fornecidos pelo provedor, o WMI atende a essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="93197-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="93197-119">O provedor também pode contar com o WMI para dar suporte à notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="93197-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="93197-120">No entanto, como um provedor Push é atualizado somente durante a inicialização, qualquer alteração em uma classe pode não ser refletida no repositório WMI por algum tempo.</span><span class="sxs-lookup"><span data-stu-id="93197-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="93197-121">Portanto, o modelo de provedor Push funciona melhor com classes que mudam pouco ou são completamente estáticas.</span><span class="sxs-lookup"><span data-stu-id="93197-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



