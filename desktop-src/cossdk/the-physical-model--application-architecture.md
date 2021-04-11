---
description: Depois que os modelos conceitual e lógico estiverem concluídos, você poderá tomar decisões sobre a implementação física do aplicativo.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'O modelo físico: arquitetura de aplicativo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089567"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="15981-103">O modelo físico: arquitetura de aplicativo</span><span class="sxs-lookup"><span data-stu-id="15981-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="15981-104">Depois que os modelos conceitual e lógico estiverem concluídos, você poderá tomar decisões sobre a implementação física do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15981-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="15981-105">Para criar o modelo físico, você deve entender onde os vários serviços do aplicativo devem ser localizados e como eles devem ser implementados.</span><span class="sxs-lookup"><span data-stu-id="15981-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="15981-106">Determinar onde os vários serviços residem deve vir antes de como os serviços serão implementados.</span><span class="sxs-lookup"><span data-stu-id="15981-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="15981-107">Uma regra básica para determinar onde residem vários serviços é: colocar o componente onde ele está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="15981-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="15981-108">Se, por exemplo, um componente Exibir informações para o cliente base, ele deverá ir para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="15981-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="15981-109">Se um componente validar as informações do cliente base, ele também deverá residir no computador do cliente base.</span><span class="sxs-lookup"><span data-stu-id="15981-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="15981-110">Se um componente atualizar as informações em um banco de dados, ele deverá residir no servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="15981-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="15981-111">Há, é claro, considerações adicionais que fazem exceções a essa regra.</span><span class="sxs-lookup"><span data-stu-id="15981-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="15981-112">Problemas de desempenho e segurança também podem ditar onde um componente está localizado.</span><span class="sxs-lookup"><span data-stu-id="15981-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="15981-113">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="15981-113">Consider the following:</span></span>

-   <span data-ttu-id="15981-114">Um componente passará a ser alterado com frequência, dificultando a distribuição de atualizações?</span><span class="sxs-lookup"><span data-stu-id="15981-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="15981-115">O componente será usado por outros aplicativos, como um componente de verificação de segurança comum?</span><span class="sxs-lookup"><span data-stu-id="15981-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="15981-116">O componente faz cálculos longos ou executa funções, como impressão, que podem ser descarregadas em um servidor?</span><span class="sxs-lookup"><span data-stu-id="15981-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="15981-117">A segurança de um componente pode ser aprimorada colocando-o em um servidor?</span><span class="sxs-lookup"><span data-stu-id="15981-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="15981-118">Localizar corretamente os componentes de um aplicativo também pode isolar a equipe de desenvolvimento da recodificação dispendiosa se o sistema ou o local dos dados for alterado.</span><span class="sxs-lookup"><span data-stu-id="15981-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="15981-119">Por exemplo, ao colocar as regras de acesso a dados em uma camada de dados em vez de em procedimentos armazenados, o aplicativo é mais facilmente isolado da dependência em um DBMS específico.</span><span class="sxs-lookup"><span data-stu-id="15981-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="15981-120">Não apenas as alterações são refinadas e testadas, mas as fontes de dados podem ser alteradas e os dados podem ser distribuídos sem alterar fundamentalmente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15981-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="15981-121">Por fim, a localização de componentes deve aproveitar as eficiências do sistema.</span><span class="sxs-lookup"><span data-stu-id="15981-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="15981-122">É hora e econômico posicionar objetos comerciais em locais centralizados na rede.</span><span class="sxs-lookup"><span data-stu-id="15981-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="15981-123">Os objetos podem ser compartilhados entre aplicativos e o teste de unidade pode ser feito antes de qualquer componente ser implantado.</span><span class="sxs-lookup"><span data-stu-id="15981-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="15981-124">Os custos de manutenção também podem ser reduzidos porque as alterações de regra ocorrem apenas em um único ponto.</span><span class="sxs-lookup"><span data-stu-id="15981-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15981-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15981-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15981-126">O modelo conceitual: requisitos de aplicativo</span><span class="sxs-lookup"><span data-stu-id="15981-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="15981-127">O modelo lógico: definição e planejamento de aplicativos</span><span class="sxs-lookup"><span data-stu-id="15981-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



