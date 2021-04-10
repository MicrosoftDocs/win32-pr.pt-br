---
description: Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação.
ms.assetid: e1302449-7f80-4881-bd76-49d386bfdafb
title: Atributo de controle timepersisting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 668cabe4832e6460b4ab01fcc048e2f8e1bbdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169837"
---
# <a name="timeremaining-control-attribute"></a><span data-ttu-id="8321e-103">Atributo de controle timepersisting</span><span class="sxs-lookup"><span data-stu-id="8321e-103">TimeRemaining Control Attribute</span></span>

<span data-ttu-id="8321e-104">Esse atributo permite que um controle de texto exiba o número aproximado de minutos e segundos restantes para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="8321e-104">This attribute enables a text control to display the approximate number of minutes and seconds remaining for an installation.</span></span> <span data-ttu-id="8321e-105">Um registro passado para o controle de texto contém um inteiro que representa o número de segundos restantes.</span><span class="sxs-lookup"><span data-stu-id="8321e-105">A record passed to the text control contains one integer representing the number of seconds remaining.</span></span> <span data-ttu-id="8321e-106">O controle de texto pesquisa a [tabela UIText](uitext-table.md) em busca de uma cadeia de caracteres chamada timecontinueing e formata o inteiro em uma cadeia de caracteres apropriada que exibe minutos e segundos.</span><span class="sxs-lookup"><span data-stu-id="8321e-106">The text control searches the [UIText table](uitext-table.md) for a string named TimeRemaining and formats the integer into an appropriate string displaying minutes and seconds.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8321e-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="8321e-107">Valid Controls</span></span>

[<span data-ttu-id="8321e-108">Text</span><span class="sxs-lookup"><span data-stu-id="8321e-108">Text</span></span>](text-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="8321e-109">Sinalizadores de bits associados</span><span class="sxs-lookup"><span data-stu-id="8321e-109">Associated Bit Flags</span></span>

<span data-ttu-id="8321e-110">Este atributo não usa sinalizadores de bit.</span><span class="sxs-lookup"><span data-stu-id="8321e-110">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="8321e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8321e-111">Remarks</span></span>

<span data-ttu-id="8321e-112">Consulte [atributos de controle](control-attributes.md) e o controle que você precisa criar sob [controles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8321e-112">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



