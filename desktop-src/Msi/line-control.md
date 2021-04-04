---
description: O controle linha é uma linha horizontal.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Controle linha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661911"
---
# <a name="line-control"></a><span data-ttu-id="324ca-103">Controle linha</span><span class="sxs-lookup"><span data-stu-id="324ca-103">Line Control</span></span>

<span data-ttu-id="324ca-104">O controle linha é uma linha horizontal.</span><span class="sxs-lookup"><span data-stu-id="324ca-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="324ca-105">Atributos de controle</span><span class="sxs-lookup"><span data-stu-id="324ca-105">Control Attributes</span></span>

<span data-ttu-id="324ca-106">Você pode usar os atributos a seguir com este controle.</span><span class="sxs-lookup"><span data-stu-id="324ca-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="324ca-107">Para alterar o valor de um atributo usando um evento, assine o controle para um ControlEvent, na [tabela EventMappings](eventmapping-table.md) e liste o identificador do atributo na coluna atributo.</span><span class="sxs-lookup"><span data-stu-id="324ca-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="324ca-108">Insira o identificador do ControlEvent, na coluna de evento.</span><span class="sxs-lookup"><span data-stu-id="324ca-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="324ca-109">Identificador de atributo</span><span class="sxs-lookup"><span data-stu-id="324ca-109">Attribute identifier</span></span>                       | <span data-ttu-id="324ca-110">Bit hexadecimal</span><span class="sxs-lookup"><span data-stu-id="324ca-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="324ca-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="324ca-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="324ca-112">Posição</span><span class="sxs-lookup"><span data-stu-id="324ca-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="324ca-113">Posição do controle na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="324ca-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="324ca-114">Insira a largura, a altura e as coordenadas do controle do canto esquerdo do controle nas colunas largura, altura, X e Y da tabela de [controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="324ca-115">Use [unidades de instalador](installer-units.md) para duração e distância.</span><span class="sxs-lookup"><span data-stu-id="324ca-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="324ca-116">Visível</span><span class="sxs-lookup"><span data-stu-id="324ca-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="324ca-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="324ca-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="324ca-118">Controle oculto.</span><span class="sxs-lookup"><span data-stu-id="324ca-118">Hidden control.</span></span> <span data-ttu-id="324ca-119">Controle visível.</span><span class="sxs-lookup"><span data-stu-id="324ca-119">Visible control.</span></span><br/> <span data-ttu-id="324ca-120">Inclua esse bit na palavra de bits da coluna atributos na tabela de [controle](control-table.md) ou na [tabela BBControl](bbcontrol-table.md) para tornar o controle visível ou oculto após sua criação.</span><span class="sxs-lookup"><span data-stu-id="324ca-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="324ca-121">Você também pode ocultar ou mostrar um controle usando a [tabela ControlCondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="324ca-122">Submersa</span><span class="sxs-lookup"><span data-stu-id="324ca-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="324ca-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="324ca-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="324ca-124">Exibe o estilo visual padrão.</span><span class="sxs-lookup"><span data-stu-id="324ca-124">Displays the default visual style.</span></span> <span data-ttu-id="324ca-125">Exibe o controle com uma aparência de baixo e 3-D.</span><span class="sxs-lookup"><span data-stu-id="324ca-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="324ca-126">Inclua esses bits na palavra de bits na coluna atributos da tabela de [controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="324ca-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="324ca-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="324ca-127">Remarks</span></span>

<span data-ttu-id="324ca-128">Esse controle pode ser criado a partir da classe estática usando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="324ca-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="324ca-129">Ele tem os estilos **SS \_ ETCHEDHORZ** e **SS \_ relevo** .</span><span class="sxs-lookup"><span data-stu-id="324ca-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
