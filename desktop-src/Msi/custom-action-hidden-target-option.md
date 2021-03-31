---
description: Use os sinalizadores de opção a seguir para especificar que o instalador não grave o valor inserido no campo de destino da tabela CustomAction no log. Para definir a opção, adicione o valor nessa tabela ao valor no campo tipo da tabela CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opção de destino oculto de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011159"
---
# <a name="custom-action-hidden-target-option"></a><span data-ttu-id="456ec-104">Opção de destino oculto de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="456ec-104">Custom Action Hidden Target Option</span></span>

<span data-ttu-id="456ec-105">Use os sinalizadores de opção a seguir para especificar que o instalador não grave o valor inserido no campo de destino da [tabela CustomAction](customaction-table.md) no log.</span><span class="sxs-lookup"><span data-stu-id="456ec-105">Use the following option flags to specify that the installer not write the value entered into the Target field of the [CustomAction table](customaction-table.md) into the log.</span></span> <span data-ttu-id="456ec-106">Para definir a opção, adicione o valor nessa tabela ao valor no campo tipo da tabela CustomAction.</span><span class="sxs-lookup"><span data-stu-id="456ec-106">To set the option add the value in this table to the value in the Type field of the CustomAction table.</span></span>



| <span data-ttu-id="456ec-107">Constante</span><span class="sxs-lookup"><span data-stu-id="456ec-107">Constant</span></span>                            | <span data-ttu-id="456ec-108">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="456ec-108">Hexadecimal</span></span> | <span data-ttu-id="456ec-109">Decimal</span><span class="sxs-lookup"><span data-stu-id="456ec-109">Decimal</span></span> | <span data-ttu-id="456ec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="456ec-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="456ec-111">(nenhum)</span><span class="sxs-lookup"><span data-stu-id="456ec-111">(none)</span></span>                              | <span data-ttu-id="456ec-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="456ec-112">0x0000</span></span>      | <span data-ttu-id="456ec-113">0</span><span class="sxs-lookup"><span data-stu-id="456ec-113">0</span></span>       | <span data-ttu-id="456ec-114">O instalador pode gravar o valor na coluna de destino da tabela CustomAction no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="456ec-114">The installer may write the value in the Target column of the CustomAction table into the log file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="456ec-115">**msidbCustomActionTypeHideTarget**</span><span class="sxs-lookup"><span data-stu-id="456ec-115">**msidbCustomActionTypeHideTarget**</span></span> | <span data-ttu-id="456ec-116">0x2000</span><span class="sxs-lookup"><span data-stu-id="456ec-116">0x2000</span></span>      | <span data-ttu-id="456ec-117">8192</span><span class="sxs-lookup"><span data-stu-id="456ec-117">8192</span></span>    | <span data-ttu-id="456ec-118">O instalador é impedido de gravar o valor na coluna de destino da [tabela CustomAction](customaction-table.md) no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="456ec-118">The installer is prevented from writing the value in the Target column of the [CustomAction table](customaction-table.md) into the log file.</span></span> <span data-ttu-id="456ec-119">A propriedade CustomActionData também não é registrada quando o instalador executa a ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="456ec-119">The CustomActionData property is also not logged when the installer executes the custom action.</span></span><br/> <span data-ttu-id="456ec-120">Como o instalador define o valor de CustomActionData de uma propriedade com o mesmo nome que a ação personalizada, essa propriedade deve ser listada na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) para impedir que seu valor apareça no log.</span><span class="sxs-lookup"><span data-stu-id="456ec-120">Because the installer sets the value of CustomActionData from a property with the same name as the custom action, that property must be listed in the [**MsiHiddenProperties**](msihiddenproperties.md) Property to prevent its value from appearing in the log.</span></span><br/> |



 

<span data-ttu-id="456ec-121">Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md)</span><span class="sxs-lookup"><span data-stu-id="456ec-121">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="456ec-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="456ec-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="456ec-123">Referência de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="456ec-123">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="456ec-124">Sobre ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="456ec-124">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="456ec-125">Usando ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="456ec-125">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 




