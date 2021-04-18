---
description: ICE44 valida que as caixas de diálogo NewDialog, SpawnDialog e SpawnWaitDialog de referência de ControlEvents são válidas na tabela de diálogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766872"
---
# <a name="ice44"></a><span data-ttu-id="ee279-103">ICE44</span><span class="sxs-lookup"><span data-stu-id="ee279-103">ICE44</span></span>

<span data-ttu-id="ee279-104">ICE44 valida que as caixas de diálogo [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)e [SpawnWaitDialog](spawnwaitdialog-controlevent.md) de referência de ControlEvents são válidas na [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee279-104">ICE44 validates that the [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md), and [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents reference valid dialog boxes in the [Dialog table](dialog-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="ee279-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="ee279-105">Result</span></span>

<span data-ttu-id="ee279-106">ICE44 posta uma mensagem de erro se houver um evento de controle de diálogo que não faça referência a uma caixa de diálogo listada na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee279-106">ICE44 posts an error message if there is a dialog control event that does not reference a dialog box listed in the Dialog table.</span></span>

## <a name="example"></a><span data-ttu-id="ee279-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ee279-107">Example</span></span>

<span data-ttu-id="ee279-108">ICE44 relataria os erros a seguir para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="ee279-108">ICE44 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="ee279-109">Erro de ICE44</span><span class="sxs-lookup"><span data-stu-id="ee279-109">ICE44 error</span></span>                                                                                                                               | <span data-ttu-id="ee279-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee279-110">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee279-111">Evento de controle para o controle ' Dialog1 '. ' Control1 ' é do tipo SpawnDialog, mas seu argumento Dialog2 não é uma entrada válida na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee279-111">Control Event for Control 'Dialog1'.'Control1' is of type SpawnDialog, but its argument Dialog2 is not a valid entry in the Dialog Table.</span></span> | <span data-ttu-id="ee279-112">Há uma ação SpawnDialog, SpawnWaitDialog ou NewDialog que tem um argumento que não se refere a uma caixa de diálogo na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee279-112">There is a SpawnDialog, SpawnWaitDialog, or NewDialog actions that has an argument that does not refer to a dialog box in the Dialog table.</span></span> <span data-ttu-id="ee279-113">Para corrigir esse erro, adicione um argumento que seja uma chave na tabela de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee279-113">To fix this error, add an argument that is a key in the Dialog Table.</span></span><br/> |



 

<span data-ttu-id="ee279-114">[Tabela de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ee279-114">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="ee279-115">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="ee279-115">Dialog</span></span>  | <span data-ttu-id="ee279-116">Título</span><span class="sxs-lookup"><span data-stu-id="ee279-116">Title</span></span> |
|---------|-------|
| <span data-ttu-id="ee279-117">Dialog1</span><span class="sxs-lookup"><span data-stu-id="ee279-117">Dialog1</span></span> |       |



 

<span data-ttu-id="ee279-118">[Tabela ControlEvent,](controlevent-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="ee279-118">[ControlEvent Table](controlevent-table.md) (partial)</span></span>



| <span data-ttu-id="ee279-119">caixa de diálogo\_</span><span class="sxs-lookup"><span data-stu-id="ee279-119">Dialog\_</span></span> | <span data-ttu-id="ee279-120">controle\_</span><span class="sxs-lookup"><span data-stu-id="ee279-120">Control\_</span></span> | <span data-ttu-id="ee279-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee279-121">Type</span></span>        | <span data-ttu-id="ee279-122">Argumento</span><span class="sxs-lookup"><span data-stu-id="ee279-122">Argument</span></span> |
|----------|-----------|-------------|----------|
| <span data-ttu-id="ee279-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="ee279-123">Dialog1</span></span>  | <span data-ttu-id="ee279-124">Control1</span><span class="sxs-lookup"><span data-stu-id="ee279-124">Control1</span></span>  | <span data-ttu-id="ee279-125">SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="ee279-125">SpawnDialog</span></span> | <span data-ttu-id="ee279-126">Dialog2</span><span class="sxs-lookup"><span data-stu-id="ee279-126">Dialog2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ee279-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee279-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee279-128">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="ee279-128">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




