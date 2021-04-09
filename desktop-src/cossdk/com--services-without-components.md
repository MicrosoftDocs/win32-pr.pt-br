---
description: Serviços COM+ sem componentes
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Serviços COM+ sem componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089317"
---
# <a name="com-services-without-components"></a><span data-ttu-id="2d439-103">Serviços COM+ sem componentes</span><span class="sxs-lookup"><span data-stu-id="2d439-103">COM+ Services Without Components</span></span>

<span data-ttu-id="2d439-104">Com o COM+ 1,5, você pode usar os serviços fornecidos pelo COM+ sem a necessidade de criar um componente para conter os métodos que chamam esses serviços.</span><span class="sxs-lookup"><span data-stu-id="2d439-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="2d439-105">Isso beneficia muito os desenvolvedores que normalmente não usam componentes, mas desejam usar serviços COM+, como transações ou o controlador COM+.</span><span class="sxs-lookup"><span data-stu-id="2d439-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="2d439-106">Usando serviços COM+ sem componentes, os desenvolvedores podem evitar a sobrecarga de criar um componente que é usado para acessar apenas os serviços COM+ de que precisam.</span><span class="sxs-lookup"><span data-stu-id="2d439-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="2d439-107">Por exemplo, ambientes de script tradicionalmente têm sido os maiores consumidores de serviços COM+, mas nunca podiam usar esses serviços com eficiência, pois os serviços precisavam ser agrupados em um componente COM+.</span><span class="sxs-lookup"><span data-stu-id="2d439-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="2d439-108">Esse requisito de agrupamento aumentou os custos de desempenho devido à maior comunicação e duplicação de dados necessários para que o ambiente de script interaja com o componente.</span><span class="sxs-lookup"><span data-stu-id="2d439-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="2d439-109">Usando serviços sem componentes, esses custos são minimizados.</span><span class="sxs-lookup"><span data-stu-id="2d439-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="2d439-110">Os tópicos descritos na tabela a seguir fornecem informações em segundo plano e tarefas sobre como usar serviços COM+ sem componentes.</span><span class="sxs-lookup"><span data-stu-id="2d439-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="2d439-111">Esse recurso destina-se a desenvolvedores de Visual C++ avançados que se preocupam com o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2d439-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="2d439-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="2d439-112">Topic</span></span>                                                                                                 | <span data-ttu-id="2d439-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d439-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d439-114">Conceitos dos serviços COM+ sem componentes</span><span class="sxs-lookup"><span data-stu-id="2d439-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="2d439-115">Fornece uma visão geral do uso dos serviços COM+ sem componentes.</span><span class="sxs-lookup"><span data-stu-id="2d439-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="2d439-116">Serviços COM+ sem tarefas de componentes</span><span class="sxs-lookup"><span data-stu-id="2d439-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="2d439-117">Fornece instruções para usar o COM+ para criar e usar serviços sem componentes.</span><span class="sxs-lookup"><span data-stu-id="2d439-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




