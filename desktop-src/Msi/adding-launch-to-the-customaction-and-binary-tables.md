---
description: Adicione um registro à tabela CustomAction para a ação personalizada de inicialização.
ms.assetid: 010ce7cd-010b-4fac-90ad-5745c6a38630
title: Adicionando inicialização às tabelas CustomAction e binary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbcd1b483505d7d33981d695ed0d29c3b72a3f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091549"
---
# <a name="adding-launch-to-the-customaction-and-binary-tables"></a><span data-ttu-id="2324d-103">Adicionando inicialização às tabelas CustomAction e binary</span><span class="sxs-lookup"><span data-stu-id="2324d-103">Adding Launch to the CustomAction and Binary Tables</span></span>

<span data-ttu-id="2324d-104">Adicione um registro à [tabela CustomAction](customaction-table.md) para a ação personalizada de inicialização.</span><span class="sxs-lookup"><span data-stu-id="2324d-104">Add a record to the [CustomAction table](customaction-table.md) for the Launch custom action.</span></span> <span data-ttu-id="2324d-105">Insira o nome da ação personalizada na coluna ação da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="2324d-105">Enter the custom action's name in the Action column of the CustomAction table.</span></span> <span data-ttu-id="2324d-106">Insira o tipo numérico total para inicialização, 65, na coluna tipo da tabela ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="2324d-106">Enter the total numeric type for Launch, 65, into the Type column of the Custom action table.</span></span> <span data-ttu-id="2324d-107">A coluna Source da tabela CustomAction especifica uma chave para o registro da [tabela binária](binary-table.md) que contém os dados binários da dll.</span><span class="sxs-lookup"><span data-stu-id="2324d-107">The Source column of the CustomAction table specifies a key into the record of the [Binary Table](binary-table.md) that contains the binary data for the DLL.</span></span> <span data-ttu-id="2324d-108">Insira Tutorial.dll na coluna de origem da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="2324d-108">Enter Tutorial.dll into the Source column of the CustomAction table.</span></span> <span data-ttu-id="2324d-109">O ponto de entrada especificado no campo de destino da tabela CustomAction deve corresponder ao exportado da DLL.</span><span class="sxs-lookup"><span data-stu-id="2324d-109">The entry point specified in the Target field of the CustomAction table must match that exported from the DLL.</span></span> <span data-ttu-id="2324d-110">Insira LaunchTutorial na coluna de destino da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="2324d-110">Enter LaunchTutorial into the Target column of the CustomAction table.</span></span>

[<span data-ttu-id="2324d-111">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="2324d-111">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="2324d-112">Ação</span><span class="sxs-lookup"><span data-stu-id="2324d-112">Action</span></span> | <span data-ttu-id="2324d-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2324d-113">Type</span></span> | <span data-ttu-id="2324d-114">Fonte</span><span class="sxs-lookup"><span data-stu-id="2324d-114">Source</span></span>       | <span data-ttu-id="2324d-115">Destino</span><span class="sxs-lookup"><span data-stu-id="2324d-115">Target</span></span>         |
|--------|------|--------------|----------------|
| <span data-ttu-id="2324d-116">Inicializar</span><span class="sxs-lookup"><span data-stu-id="2324d-116">Launch</span></span> | <span data-ttu-id="2324d-117">65</span><span class="sxs-lookup"><span data-stu-id="2324d-117">65</span></span>   | <span data-ttu-id="2324d-118">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="2324d-118">Tutorial.dll</span></span> | <span data-ttu-id="2324d-119">LaunchTutorial</span><span class="sxs-lookup"><span data-stu-id="2324d-119">LaunchTutorial</span></span> |



 

<span data-ttu-id="2324d-120">Adicione o Tutorial.dll criado no tutorial. cpp como um fluxo binário à tabela binária.</span><span class="sxs-lookup"><span data-stu-id="2324d-120">Add the Tutorial.dll you created from Tutorial.cpp as a binary stream to the Binary table.</span></span>

[<span data-ttu-id="2324d-121">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="2324d-121">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="2324d-122">Nome</span><span class="sxs-lookup"><span data-stu-id="2324d-122">Name</span></span>         | <span data-ttu-id="2324d-123">Dados</span><span class="sxs-lookup"><span data-stu-id="2324d-123">Data</span></span>                          |
|--------------|-------------------------------|
| <span data-ttu-id="2324d-124">Tutorial.dll</span><span class="sxs-lookup"><span data-stu-id="2324d-124">Tutorial.dll</span></span> | <span data-ttu-id="2324d-125">{*dados binários adicionados para dll*}</span><span class="sxs-lookup"><span data-stu-id="2324d-125">{*binary data added for DLL*}</span></span> |



 

<span data-ttu-id="2324d-126">Continue a [Adicionar um evento de controle no final da instalação para executar a inicialização](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span><span class="sxs-lookup"><span data-stu-id="2324d-126">Continue to [Adding a Control Event at the End of the Installation to Run Launch](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md).</span></span>

 

 



