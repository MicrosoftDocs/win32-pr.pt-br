---
description: A tabela de mural lista os controles de mural exibidos na interface do usuário completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabela de mural
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921485"
---
# <a name="billboard-table"></a><span data-ttu-id="40378-103">Tabela de mural</span><span class="sxs-lookup"><span data-stu-id="40378-103">Billboard Table</span></span>

<span data-ttu-id="40378-104">A tabela de mural lista os [controles de mural](billboard-control.md) exibidos na interface do usuário completa.</span><span class="sxs-lookup"><span data-stu-id="40378-104">The Billboard table lists the [Billboard controls](billboard-control.md) displayed in the full user interface.</span></span>

<span data-ttu-id="40378-105">A tabela de mural tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="40378-105">The Billboard table has the following columns.</span></span>



| <span data-ttu-id="40378-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="40378-106">Column</span></span>    | <span data-ttu-id="40378-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="40378-107">Type</span></span>                         | <span data-ttu-id="40378-108">Chave</span><span class="sxs-lookup"><span data-stu-id="40378-108">Key</span></span> | <span data-ttu-id="40378-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="40378-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="40378-110">Mensagem</span><span class="sxs-lookup"><span data-stu-id="40378-110">Billboard</span></span> | [<span data-ttu-id="40378-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="40378-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="40378-112">S</span><span class="sxs-lookup"><span data-stu-id="40378-112">Y</span></span>   | <span data-ttu-id="40378-113">N</span><span class="sxs-lookup"><span data-stu-id="40378-113">N</span></span>        |
| <span data-ttu-id="40378-114">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="40378-114">Feature\_</span></span> | [<span data-ttu-id="40378-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="40378-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="40378-116">N</span><span class="sxs-lookup"><span data-stu-id="40378-116">N</span></span>   | <span data-ttu-id="40378-117">N</span><span class="sxs-lookup"><span data-stu-id="40378-117">N</span></span>        |
| <span data-ttu-id="40378-118">Ação</span><span class="sxs-lookup"><span data-stu-id="40378-118">Action</span></span>    | [<span data-ttu-id="40378-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="40378-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="40378-120">N</span><span class="sxs-lookup"><span data-stu-id="40378-120">N</span></span>   | <span data-ttu-id="40378-121">S</span><span class="sxs-lookup"><span data-stu-id="40378-121">Y</span></span>        |
| <span data-ttu-id="40378-122">Ordenando</span><span class="sxs-lookup"><span data-stu-id="40378-122">Ordering</span></span>  | [<span data-ttu-id="40378-123">Inteiro</span><span class="sxs-lookup"><span data-stu-id="40378-123">Integer</span></span>](integer.md)       | <span data-ttu-id="40378-124">N</span><span class="sxs-lookup"><span data-stu-id="40378-124">N</span></span>   | <span data-ttu-id="40378-125">S</span><span class="sxs-lookup"><span data-stu-id="40378-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="40378-126">Colunas</span><span class="sxs-lookup"><span data-stu-id="40378-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="40378-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Mensagem</span><span class="sxs-lookup"><span data-stu-id="40378-127"><span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Billboard</span></span>
</dt> <dd>

<span data-ttu-id="40378-128">Nome do [controle do mural](billboard-control.md).</span><span class="sxs-lookup"><span data-stu-id="40378-128">Name of the [Billboard control](billboard-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="40378-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="40378-129"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="40378-130">Uma chave externa para a primeira coluna da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="40378-130">An external key to the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="40378-131">O mural será exibido somente se esse recurso estiver sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="40378-131">The billboard is displayed only if this feature is being installed.</span></span>

</dd> <dt>

<span data-ttu-id="40378-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span><span class="sxs-lookup"><span data-stu-id="40378-132"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="40378-133">O nome de uma ação.</span><span class="sxs-lookup"><span data-stu-id="40378-133">The name of an action.</span></span> <span data-ttu-id="40378-134">O mural é exibido durante as mensagens de andamento recebidas desta ação.</span><span class="sxs-lookup"><span data-stu-id="40378-134">The billboard is displayed during the progress messages received from this action.</span></span>

</dd> <dt>

<span data-ttu-id="40378-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenação</span><span class="sxs-lookup"><span data-stu-id="40378-135"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="40378-136">Se houver mais de um mural correspondente a uma ação, eles serão exibidos na ordem definida por esta coluna.</span><span class="sxs-lookup"><span data-stu-id="40378-136">If there is more than one billboard corresponding to an action, then they are displayed in the order defined by this column.</span></span> <span data-ttu-id="40378-137">Esse número deve ser não negativo.</span><span class="sxs-lookup"><span data-stu-id="40378-137">This number must be non-negative.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="40378-138">Validação</span><span class="sxs-lookup"><span data-stu-id="40378-138">Validation</span></span>

<dl>

[<span data-ttu-id="40378-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="40378-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="40378-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="40378-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="40378-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="40378-141">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="40378-142">ICE95</span><span class="sxs-lookup"><span data-stu-id="40378-142">ICE95</span></span>](ice95.md)  
</dl>

 

 



