---
title: Principais alterações desde o Windows 7 para garantir a compatibilidade
description: Principais alterações desde o Windows 7 para garantir a compatibilidade
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292593"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="bfa97-103">Principais alterações desde o Windows 7 para garantir a compatibilidade</span><span class="sxs-lookup"><span data-stu-id="bfa97-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="bfa97-104">Entendemos que compatibilidade é importante para os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="bfa97-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="bfa97-105">Os ISVs e desenvolvedores querem verificar se os aplicativos deles serão executados como esperado em todas as versões compatíveis do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="bfa97-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="bfa97-106">Os consumidores e as empresas têm um importante investimento aqui — eles querem a certeza de que os aplicativos pelos quais eles pagaram continuarão funcionando.</span><span class="sxs-lookup"><span data-stu-id="bfa97-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="bfa97-107">Nós sabemos que compatibilidade é o principal critério para decisões de compra.</span><span class="sxs-lookup"><span data-stu-id="bfa97-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="bfa97-108">Os aplicativos que são bem escritos com base nas práticas recomendadas levarão a uma variação muito menor de código quando uma nova versão do Windows for lançada e reduzirá a fragmentação — esses aplicativos têm um investimento de engenharia reduzido para serem mantidos e um tempo de comercialização mais rápido.</span><span class="sxs-lookup"><span data-stu-id="bfa97-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="bfa97-109">No cronograma do Windows 7, compatibilidade era muito mais uma abordagem reativa.</span><span class="sxs-lookup"><span data-stu-id="bfa97-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="bfa97-110">No Windows 8, começamos a observar isso de forma diferente, trabalhando dentro do Windows para garantir que a compatibilidade foi projetada no lugar de ser considerada algo secundário.</span><span class="sxs-lookup"><span data-stu-id="bfa97-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="bfa97-111">Windows 10 é a versão mais compatível por design do sistema operacional até a data.</span><span class="sxs-lookup"><span data-stu-id="bfa97-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="bfa97-112">Veja algumas importantes maneiras por meio das quais conseguimos isso:</span><span class="sxs-lookup"><span data-stu-id="bfa97-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="bfa97-113">Telemetria de aplicativos: isso nos ajuda a entender a popularidade do aplicativo no ecossistema do Windows para informar os testes de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="bfa97-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="bfa97-114">Parcerias ISV: trabalhe diretamente com parceiros externos para fornecer dados e ajudar a corrigir problemas que nossos usuários têm experiência.</span><span class="sxs-lookup"><span data-stu-id="bfa97-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="bfa97-115">Análises de design, detecção de upstream: parceiro com equipes de recursos para reduzir o número de alterações significativas no Windows.</span><span class="sxs-lookup"><span data-stu-id="bfa97-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="bfa97-116">A análise de compatibilidade é uma entrada pela qual as nossas equipes de recurso devem passar.</span><span class="sxs-lookup"><span data-stu-id="bfa97-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="bfa97-117">Controle mais rígido sobre as alterações de API & comunicação aprimorada</span><span class="sxs-lookup"><span data-stu-id="bfa97-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="bfa97-118">Loop de voo e comentários: a população do Windows Insider recebe compilações comprovadas que ajudam a melhorar nossa capacidade de encontrar problemas de compatibilidade antes que uma compilação final seja lançada para os clientes.</span><span class="sxs-lookup"><span data-stu-id="bfa97-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="bfa97-119">Esse processo de comentários não só expõe os bugs, mas verifica se entregamos os recursos que nossos usuários querem.</span><span class="sxs-lookup"><span data-stu-id="bfa97-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




