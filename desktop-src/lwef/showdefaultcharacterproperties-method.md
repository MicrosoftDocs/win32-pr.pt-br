---
title: Método ShowDefaultCharacterProperties
description: Método ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635706"
---
# <a name="showdefaultcharacterproperties-method"></a><span data-ttu-id="43009-103">Método ShowDefaultCharacterProperties</span><span class="sxs-lookup"><span data-stu-id="43009-103">ShowDefaultCharacterProperties Method</span></span>

<span data-ttu-id="43009-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43009-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="43009-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="43009-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="43009-106">Exibe as propriedades do caractere padrão.</span><span class="sxs-lookup"><span data-stu-id="43009-106">Displays the default character's properties.</span></span>

</dd> <dt>

<span data-ttu-id="43009-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="43009-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="43009-108">\*Agent \* \* *. ShowDefaultCharacterProperties* \*  \[ *X* , *Y*\]</span><span class="sxs-lookup"><span data-stu-id="43009-108">*agent\*\*\*.ShowDefaultCharacterProperties*\* \[ *X* , *Y* \]</span></span>



| <span data-ttu-id="43009-109">Parte</span><span class="sxs-lookup"><span data-stu-id="43009-109">Part</span></span> | <span data-ttu-id="43009-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="43009-110">Description</span></span>                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43009-111">*X*</span><span class="sxs-lookup"><span data-stu-id="43009-111">*X*</span></span>  | <span data-ttu-id="43009-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="43009-112">Optional.</span></span> <span data-ttu-id="43009-113">Um valor inteiro curto que indica a coordenada de tela horizontal (*X* ) para exibir a janela.</span><span class="sxs-lookup"><span data-stu-id="43009-113">A short integer value that indicates the horizontal (*X* ) screen coordinate to display the window.</span></span> <span data-ttu-id="43009-114">Essa coordenada deve ser especificada em pixels.</span><span class="sxs-lookup"><span data-stu-id="43009-114">This coordinate must be specified in pixels.</span></span> |
| <span data-ttu-id="43009-115">*S*</span><span class="sxs-lookup"><span data-stu-id="43009-115">*Y*</span></span>  | <span data-ttu-id="43009-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="43009-116">Optional.</span></span> <span data-ttu-id="43009-117">Um valor inteiro curto que indica a coordenada de tela vertical (*Y*) para exibir a janela.</span><span class="sxs-lookup"><span data-stu-id="43009-117">A short integer value that indicates the vertical (*Y*) screen coordinate to display the window.</span></span> <span data-ttu-id="43009-118">Essa coordenada deve ser especificada em pixels.</span><span class="sxs-lookup"><span data-stu-id="43009-118">This coordinate must be specified in pixels.</span></span>    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43009-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="43009-119">Remarks</span></span>

<span data-ttu-id="43009-120">Chamar esse método exibe a janela Propriedades de caractere padrão (não a folha de propriedades do Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="43009-120">Calling this method displays the default character properties window (not the Microsoft Agent property sheet).</span></span> <span data-ttu-id="43009-121">Se você não especificar as coordenadas X e Y, a janela será exibida no último local em que foi exibida.</span><span class="sxs-lookup"><span data-stu-id="43009-121">If you do not specify the X and Y coordinates, the window appears at the last location it was displayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="43009-122">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="43009-122">See Also</span></span>

[<span data-ttu-id="43009-123">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="43009-123">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




