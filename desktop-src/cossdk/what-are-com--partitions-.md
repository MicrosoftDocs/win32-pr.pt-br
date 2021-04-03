---
description: Uma partição COM+ é um contêiner lógico que permite que os aplicativos sejam executados independentemente de outras configurações desses aplicativos.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: O que são partições COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104091859"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="30fa1-103">O que são partições COM+?</span><span class="sxs-lookup"><span data-stu-id="30fa1-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="30fa1-104">Uma partição COM+ é um contêiner lógico que permite que os aplicativos sejam executados independentemente de outras configurações desses aplicativos.</span><span class="sxs-lookup"><span data-stu-id="30fa1-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="30fa1-105">Cada configuração de um aplicativo é instalada em uma partição separada e pode ser gerenciada separadamente, de acordo com as necessidades específicas de seus usuários.</span><span class="sxs-lookup"><span data-stu-id="30fa1-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="30fa1-106">Durante a ativação de um componente COM+, o serviço de partições determina qual configuração do componente será ativada, com base na identidade do usuário que está solicitando a ativação do componente.</span><span class="sxs-lookup"><span data-stu-id="30fa1-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="30fa1-107">Por exemplo, uma única organização que tem dois grupos separados, produção e treinamento, pode implementar partições COM+ como uma maneira de permitir que os dois grupos usem configurações diferentes de um aplicativo COM+ no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="30fa1-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="30fa1-108">**Windows XP:** A capacidade de criar, configurar ou delegar partições COM+ não está disponível.</span><span class="sxs-lookup"><span data-stu-id="30fa1-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="30fa1-109">A partição global é a única partição COM+ disponível.</span><span class="sxs-lookup"><span data-stu-id="30fa1-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="30fa1-110">**Windows 2000:** O serviço de partições COM+ não está disponível no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="30fa1-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="30fa1-111">Benefícios do uso de partições COM+</span><span class="sxs-lookup"><span data-stu-id="30fa1-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="30fa1-112">O uso de partições COM+ oferece várias vantagens, incluindo as seguintes:</span><span class="sxs-lookup"><span data-stu-id="30fa1-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="30fa1-113">As organizações podem reduzir o TCO (custo total de propriedade) usando menos servidores de aplicativos físicos para dar suporte a usuários que precisam de várias configurações de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="30fa1-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="30fa1-114">A sobrecarga administrativa é reduzida.</span><span class="sxs-lookup"><span data-stu-id="30fa1-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="30fa1-115">Em vez de configurar e gerenciar vários computadores, os administradores precisam apenas configurar e gerenciar várias partições no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="30fa1-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="30fa1-116">Além disso, as partições podem ser gerenciadas programaticamente por meio da adição de uma nova interface de programação COM+.</span><span class="sxs-lookup"><span data-stu-id="30fa1-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="30fa1-117">A segurança pode ser implementada e gerenciada em uma base partição por partição para usuários locais, usuários de domínio e UOs (unidades organizacionais).</span><span class="sxs-lookup"><span data-stu-id="30fa1-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="30fa1-118">Os programadores e administradores podem usar as ferramentas administrativas e de desenvolvimento da Microsoft, como o SDK do Windows, Active Directory usuários e computadores e a ferramenta administrativa serviços de componentes — para gerenciar partições COM+.</span><span class="sxs-lookup"><span data-stu-id="30fa1-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="30fa1-119">O recurso de partições é totalmente integrado a essas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="30fa1-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="30fa1-120">Cenário de uso primário</span><span class="sxs-lookup"><span data-stu-id="30fa1-120">Primary Usage Scenario</span></span>

<span data-ttu-id="30fa1-121">Um dos principais motivos para os clientes implantarem o recurso de partições COM+ é hospedar aplicativos baseados na Web.</span><span class="sxs-lookup"><span data-stu-id="30fa1-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="30fa1-122">Por exemplo, suponha que uma pequena empresa de software desenvolve um aplicativo COM+ para uso pelo pessoal do hospital.</span><span class="sxs-lookup"><span data-stu-id="30fa1-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="30fa1-123">O aplicativo, que é um aplicativo baseado na Web distribuído, fornece uma maneira para que os hospitais armazenem e recuperem registros médicos de pacientes usando um banco de dados SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30fa1-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="30fa1-124">Suponha que a empresa de software tenha três clientes: hospital A, hospital B e hospital C. Enquanto cada cliente executa o lado do cliente do aplicativo COM+ localmente em seus computadores desktop, o lado do servidor do aplicativo COM+ reside no servidor Web interno da empresa de software e é acessado por seus clientes por meio da Web.</span><span class="sxs-lookup"><span data-stu-id="30fa1-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="30fa1-125">Como cada hospital tem seu próprio conjunto de requisitos de armazenamento e recuperação e seu próprio conjunto de dados de pacientes personalizados, a empresa de software deve fornecer uma maneira para que várias configurações da parte do servidor do aplicativo sejam executadas simultaneamente no servidor Web.</span><span class="sxs-lookup"><span data-stu-id="30fa1-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="30fa1-126">As partições COM+ fornecem uma solução para esse problema.</span><span class="sxs-lookup"><span data-stu-id="30fa1-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="30fa1-127">A ilustração a seguir mostra o cenário de partições para o aplicativo COM+ da empresa de software.</span><span class="sxs-lookup"><span data-stu-id="30fa1-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Diagrama que mostra um cenário de partições para um aplicativo COM+, com um aplicativo cliente para o aplicativo de servidor para o banco de dados do SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="30fa1-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30fa1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30fa1-130">Restrições de design de aplicativo</span><span class="sxs-lookup"><span data-stu-id="30fa1-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="30fa1-131">Componentes e partições em fila COM+</span><span class="sxs-lookup"><span data-stu-id="30fa1-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="30fa1-132">Implementação de partição</span><span class="sxs-lookup"><span data-stu-id="30fa1-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="30fa1-133">Registrando e ativando componentes em partições</span><span class="sxs-lookup"><span data-stu-id="30fa1-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



