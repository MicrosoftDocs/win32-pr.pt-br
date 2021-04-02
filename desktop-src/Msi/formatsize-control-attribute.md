---
description: Se esse bit for definido para um controle de texto estático, o controle tentará formatar automaticamente o texto exibido como um número que representa uma contagem de bytes.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatar atributo de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164998"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="186d7-103">Formatar atributo de controle</span><span class="sxs-lookup"><span data-stu-id="186d7-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="186d7-104">Se esse bit for definido para um controle de texto estático, o controle tentará formatar automaticamente o texto exibido como um número que representa uma contagem de bytes.</span><span class="sxs-lookup"><span data-stu-id="186d7-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="186d7-105">Para formatação adequada, o texto do controle deve ser definido como uma cadeia de caracteres que representa um número expresso em unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="186d7-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="186d7-106">Em seguida, o valor exibido é formatado em kilobytes (KB), megabytes (MB) ou gigabytes (GB) e exibido com a cadeia de caracteres apropriada que representa as unidades.</span><span class="sxs-lookup"><span data-stu-id="186d7-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="186d7-107">Para obter mais informações, consulte [controle de texto](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="186d7-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="186d7-108">Valor numérico do texto original</span><span class="sxs-lookup"><span data-stu-id="186d7-108">Numerical value of original text</span></span> | <span data-ttu-id="186d7-109">Cadeia de caracteres de unidade usada</span><span class="sxs-lookup"><span data-stu-id="186d7-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="186d7-110">Menos de 20480</span><span class="sxs-lookup"><span data-stu-id="186d7-110">Less than 20480</span></span>                  | <span data-ttu-id="186d7-111">KB</span><span class="sxs-lookup"><span data-stu-id="186d7-111">KB</span></span>               |
| <span data-ttu-id="186d7-112">Menos de 20971520</span><span class="sxs-lookup"><span data-stu-id="186d7-112">Less than 20971520</span></span>               | <span data-ttu-id="186d7-113">MB</span><span class="sxs-lookup"><span data-stu-id="186d7-113">MB</span></span>               |
| <span data-ttu-id="186d7-114">Menos de 10737418240</span><span class="sxs-lookup"><span data-stu-id="186d7-114">Less than 10737418240</span></span>            | <span data-ttu-id="186d7-115">GB</span><span class="sxs-lookup"><span data-stu-id="186d7-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="186d7-116">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="186d7-116">Valid Controls</span></span>



| <span data-ttu-id="186d7-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="186d7-117">Decimal</span></span> | <span data-ttu-id="186d7-118">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="186d7-118">Hexadecimal</span></span> | <span data-ttu-id="186d7-119">Control</span><span class="sxs-lookup"><span data-stu-id="186d7-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="186d7-120">524288</span><span class="sxs-lookup"><span data-stu-id="186d7-120">524288</span></span>  | <span data-ttu-id="186d7-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="186d7-121">0x00080000</span></span>  | <span data-ttu-id="186d7-122">msidbControlAttributesFormatSize</span><span class="sxs-lookup"><span data-stu-id="186d7-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="186d7-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="186d7-123">Remarks</span></span>

<span data-ttu-id="186d7-124">Para definir esse atributo em um controle, inclua os bits de formatação na coluna atributos do registro do controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="186d7-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="186d7-125">O texto do controle deve ser definido como uma cadeia de caracteres que representa um número expresso em unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="186d7-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="186d7-126">O texto das cadeias de caracteres de unidade é definido na [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="186d7-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="186d7-127">O posicionamento da cadeia de caracteres de unidade é controlado pela propriedade [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="186d7-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="186d7-128">Se a propriedade **LeftUnit** for definida como qualquer valor, a cadeia de caracteres de unidade será exibida antes do valor numérico.</span><span class="sxs-lookup"><span data-stu-id="186d7-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="186d7-129">Se algo diferente de caracteres numéricos aparecer no texto associado ao controle, o valor exibido será indefinido.</span><span class="sxs-lookup"><span data-stu-id="186d7-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="186d7-130">Em tempo de execução, o instalador resolve a propriedade [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) para o número total de bytes necessários para a instalação em unidades de 512.</span><span class="sxs-lookup"><span data-stu-id="186d7-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="186d7-131">Um controle de texto estático com um bit de formatação pode ser usado para formatar e rotular automaticamente o número total de bytes necessários para a instalação em KB, MB ou GB, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="186d7-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="186d7-132">Para os fins deste exemplo, suponha que o número total de bytes seja 18.336.768.</span><span class="sxs-lookup"><span data-stu-id="186d7-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="186d7-133">O instalador define o valor da propriedade PrimaryVolumeSpaceRequired como 18.336.768 dividido por 512 ou 35.814.</span><span class="sxs-lookup"><span data-stu-id="186d7-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="186d7-134">O número exibido pelo controle de texto com Formatize seria 17MB.</span><span class="sxs-lookup"><span data-stu-id="186d7-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="186d7-135">Os valores numéricos do texto original são fornecidos em unidades de 512.</span><span class="sxs-lookup"><span data-stu-id="186d7-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="186d7-136">Na tabela acima, a cadeia de caracteres 20.480 corresponde à cadeia de caracteres KB porque 20.480 vezes 512 gera um resultado de 10.485.760 bytes ou 10.240 KB.</span><span class="sxs-lookup"><span data-stu-id="186d7-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="186d7-137">As cadeias de caracteres de unidade listadas na tabela anterior referem-se às chaves na [tabela UIText](uitext-table.md), em que o texto da cadeia de caracteres da unidade é definido.</span><span class="sxs-lookup"><span data-stu-id="186d7-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="186d7-138">O posicionamento da cadeia de caracteres de unidade é controlado pela propriedade [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="186d7-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="186d7-139">Se a propriedade **LeftUnit** for definida como qualquer valor, a cadeia de caracteres de unidade será exibida antes do valor numérico.</span><span class="sxs-lookup"><span data-stu-id="186d7-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="186d7-140">Se algo diferente de caracteres numéricos aparecer no texto associado ao controle, o valor exibido será indefinido.</span><span class="sxs-lookup"><span data-stu-id="186d7-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="186d7-141">Para obter mais informações, consulte [controlar atributos](control-attributes.md) e [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="186d7-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



