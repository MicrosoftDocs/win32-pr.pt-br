---
description: ICE82 valida que a ação RegisterProduct, a ação RegisterUser, a ação PublishProduct e a ação PublishFeatures estão presentes na tabela InstallExecuteSequence. O pacote será validado se todas as ações estiverem presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662793"
---
# <a name="ice82"></a><span data-ttu-id="6bef9-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="6bef9-104">ICE82</span></span>

<span data-ttu-id="6bef9-105">ICE82 valida que a ação [RegisterProduct](registerproduct-action.md), a ação [RegisterUser](registeruser-action.md), a [ação PublishProduct](publishproduct-action.md)e a [ação PublishFeatures](publishfeatures-action.md) estão presentes na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6bef9-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="6bef9-106">O pacote será validado se todas as ações estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="6bef9-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="6bef9-107">ICE82 posta um aviso se houver duas ações com o mesmo número de sequência listado nas tabelas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6bef9-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="6bef9-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="6bef9-108">Result</span></span>

<span data-ttu-id="6bef9-109">ICE82 posta os seguintes avisos.</span><span class="sxs-lookup"><span data-stu-id="6bef9-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="6bef9-110">Aviso de ICE82</span><span class="sxs-lookup"><span data-stu-id="6bef9-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="6bef9-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bef9-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bef9-112">A tabela InstallExecuteSequence não contém o conjunto de ações mencionadas abaixo: ações ausentes:</span><span class="sxs-lookup"><span data-stu-id="6bef9-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="6bef9-113">Recursos de publicação</span><span class="sxs-lookup"><span data-stu-id="6bef9-113">Publish Features</span></span><br/> <span data-ttu-id="6bef9-114">Publicar produto</span><span class="sxs-lookup"><span data-stu-id="6bef9-114">Publish Product</span></span><br/> <span data-ttu-id="6bef9-115">Registrar produto</span><span class="sxs-lookup"><span data-stu-id="6bef9-115">Register Product</span></span><br/> <span data-ttu-id="6bef9-116">Registrar usuário</span><span class="sxs-lookup"><span data-stu-id="6bef9-116">Register User</span></span><br/> | <span data-ttu-id="6bef9-117">ICE82 ação personalizada postará um aviso se todas as quatro ações estiverem ausentes.</span><span class="sxs-lookup"><span data-stu-id="6bef9-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="6bef9-118">Esta ação \[ 1 \] tem o número de sequência duplicado \[ 2 \] na tabela \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="6bef9-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="6bef9-119">ICE82 posta um aviso se houver duas ações com o mesmo número de sequência listado nas tabelas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="6bef9-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="6bef9-120">ICE82 posta os erros a seguir.</span><span class="sxs-lookup"><span data-stu-id="6bef9-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="6bef9-121">Erro de ICE82</span><span class="sxs-lookup"><span data-stu-id="6bef9-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="6bef9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bef9-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6bef9-123">O InstallExecuteSequence deve conter todas as ações mencionadas abaixo ou nenhuma dessas ações presentes</span><span class="sxs-lookup"><span data-stu-id="6bef9-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="6bef9-124">Ações ausentes:</span><span class="sxs-lookup"><span data-stu-id="6bef9-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="6bef9-125">ICE82 lançará um erro se algumas das quatro ações estiverem presentes e outras estiverem ausentes.</span><span class="sxs-lookup"><span data-stu-id="6bef9-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6bef9-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6bef9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bef9-127">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="6bef9-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




