---
description: O controle de mural exibe controles comumente usados que são adicionados e removidos da caixa de diálogo por ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Controle de mural
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828054"
---
# <a name="billboard-control"></a><span data-ttu-id="ee43b-103">Controle de mural</span><span class="sxs-lookup"><span data-stu-id="ee43b-103">Billboard Control</span></span>

<span data-ttu-id="ee43b-104">O controle de mural exibe controles comumente usados que são adicionados e removidos da caixa de diálogo por ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="ee43b-104">The Billboard control displays commonly used controls that are added and removed from the dialog box by ControlEvents.</span></span> <span data-ttu-id="ee43b-105">Somente controles que não estão associados a uma propriedade, como [texto](text-control.md), [bitmap](bitmap-control.md)ou [ícone](icon-control.md), ou controles personalizados, podem ser colocados em um mural.</span><span class="sxs-lookup"><span data-stu-id="ee43b-105">Only controls that are not associated with a property, such as [Text](text-control.md), [Bitmap](bitmap-control.md), or [Icon](icon-control.md), or custom controls can be placed on a billboard.</span></span> <span data-ttu-id="ee43b-106">Os controles de mensagem geralmente exibem mensagens de progresso.</span><span class="sxs-lookup"><span data-stu-id="ee43b-106">Billboard controls most typically display progress messages.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="ee43b-107">Atributos de controle</span><span class="sxs-lookup"><span data-stu-id="ee43b-107">Control Attributes</span></span>

<span data-ttu-id="ee43b-108">Você pode usar os atributos a seguir com o controle de mural.</span><span class="sxs-lookup"><span data-stu-id="ee43b-108">You can use the following attributes with the Billboard control.</span></span> <span data-ttu-id="ee43b-109">Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo.</span><span class="sxs-lookup"><span data-stu-id="ee43b-109">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="ee43b-110">Insira o identificador do ControlEvent, na coluna de evento.</span><span class="sxs-lookup"><span data-stu-id="ee43b-110">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="ee43b-111">Identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="ee43b-111">Attribute identifier</span></span>                                 | <span data-ttu-id="ee43b-112">Bit hexadecimal</span><span class="sxs-lookup"><span data-stu-id="ee43b-112">Hexadecimal bit</span></span>                  | <span data-ttu-id="ee43b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee43b-113">Description</span></span>                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee43b-114">Muralname</span><span class="sxs-lookup"><span data-stu-id="ee43b-114">BillboardName</span></span>](billboardname-control-attribute.md) |                                  | <span data-ttu-id="ee43b-115">Nome do mural atual.</span><span class="sxs-lookup"><span data-stu-id="ee43b-115">Name of the current billboard.</span></span> <span data-ttu-id="ee43b-116">Insira o identificador do mural na coluna do mural da [tabela BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-116">Enter the billboard's identifier in the Billboard column of the [BBControl table](bbcontrol-table.md).</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="ee43b-117">Posição</span><span class="sxs-lookup"><span data-stu-id="ee43b-117">Position</span></span>](position-control-attribute.md)           |                                  | <span data-ttu-id="ee43b-118">Posição de controle na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee43b-118">Position of control in the dialog box.</span></span> <span data-ttu-id="ee43b-119">Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da [tabela BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-119">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="ee43b-120">Use [unidades de instalador](installer-units.md) para duração e distância.</span><span class="sxs-lookup"><span data-stu-id="ee43b-120">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                |
| [<span data-ttu-id="ee43b-121">Visível</span><span class="sxs-lookup"><span data-stu-id="ee43b-121">Visible</span></span>](visible-control-attribute.md)             | <span data-ttu-id="ee43b-122">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="ee43b-122">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="ee43b-123">Controle oculto.</span><span class="sxs-lookup"><span data-stu-id="ee43b-123">Hidden control.</span></span> <span data-ttu-id="ee43b-124">Controle visível.</span><span class="sxs-lookup"><span data-stu-id="ee43b-124">Visible control.</span></span><br/> <span data-ttu-id="ee43b-125">Inclua esse bit na palavra de bits da coluna atributos na [tabela BBControl](bbcontrol-table.md) para tornar o controle visível ou oculto após sua criação.</span><span class="sxs-lookup"><span data-stu-id="ee43b-125">Include this bit in the bit word of the Attributes column in the [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="ee43b-126">Oculte ou mostre um controle usando a [tabela ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-126">Hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="ee43b-127">Submersa</span><span class="sxs-lookup"><span data-stu-id="ee43b-127">Sunken</span></span>](sunken-control-attribute.md)               | <span data-ttu-id="ee43b-128">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="ee43b-128">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="ee43b-129">Exibe o estilo visual padrão.</span><span class="sxs-lookup"><span data-stu-id="ee43b-129">Displays the default visual style.</span></span> <span data-ttu-id="ee43b-130">Exibe o controle com uma aparência de baixo e 3-D.</span><span class="sxs-lookup"><span data-stu-id="ee43b-130">Displays the control with a sunken, 3-D, look.</span></span><br/> <span data-ttu-id="ee43b-131">Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-131">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ee43b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee43b-132">Remarks</span></span>

<span data-ttu-id="ee43b-133">Este controle não tem nenhuma janela própria.</span><span class="sxs-lookup"><span data-stu-id="ee43b-133">This control has no window of its own.</span></span>

<span data-ttu-id="ee43b-134">Os controles de mensagem que aparecem na interface do usuário completa são listados na [tabela do mural](billboard-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-134">Billboard controls that appear in the full user interface are listed in the [Billboard table](billboard-table.md).</span></span>

<span data-ttu-id="ee43b-135">Os controles que estão localizados em um mural devem ser listados na [tabela BBControl](bbcontrol-table.md) em vez da [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee43b-135">Controls that are located on a billboard must be listed in the [BBControl table](bbcontrol-table.md) rather than the [Control table](control-table.md).</span></span>

 

 




