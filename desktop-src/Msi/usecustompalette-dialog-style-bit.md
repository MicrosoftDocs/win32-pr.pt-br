---
description: Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado). Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit de estilo de caixa de diálogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751833"
---
# <a name="usecustompalette-dialog-style-bit"></a><span data-ttu-id="8f276-104">Bit de estilo de caixa de diálogo UseCustomPalette</span><span class="sxs-lookup"><span data-stu-id="8f276-104">UseCustomPalette Dialog Style Bit</span></span>

<span data-ttu-id="8f276-105">Se esse bit for definido, as imagens na caixa de diálogo serão criadas com a paleta personalizada (uma por caixa de diálogo recebida do primeiro controle criado).</span><span class="sxs-lookup"><span data-stu-id="8f276-105">If this bit is set, the pictures on the dialog box are created with the custom palette (one per dialog received from the first control created).</span></span> <span data-ttu-id="8f276-106">Se o bit não estiver definido, as imagens serão renderizadas usando uma paleta padrão.</span><span class="sxs-lookup"><span data-stu-id="8f276-106">If the bit is not set, the pictures are rendered using a default palette.</span></span>

<span data-ttu-id="8f276-107">Normalmente, ele definiria esse bit se a caixa de diálogo contiver uma imagem com uma paleta especial ou várias imagens compartilhando uma paleta personalizada.</span><span class="sxs-lookup"><span data-stu-id="8f276-107">Typically one would set this bit if the dialog contains a picture with a special palette, or several pictures sharing a custom palette.</span></span> <span data-ttu-id="8f276-108">O bit não deverá ser definido se a caixa de diálogo contiver várias imagens com paletas diferentes.</span><span class="sxs-lookup"><span data-stu-id="8f276-108">The bit should not be set if the dialog contains several pictures with different palettes.</span></span> <span data-ttu-id="8f276-109">Nesse caso, a paleta padrão tem mais probabilidade de fornecer um resultado satisfatório para todas as imagens.</span><span class="sxs-lookup"><span data-stu-id="8f276-109">In this case, the default palette is most likely to give a satisfactory result for all pictures.</span></span>

## <a name="value"></a><span data-ttu-id="8f276-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8f276-110">Value</span></span>



| <span data-ttu-id="8f276-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="8f276-111">Decimal</span></span> | <span data-ttu-id="8f276-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="8f276-112">Hexadecimal</span></span> | <span data-ttu-id="8f276-113">Constante</span><span class="sxs-lookup"><span data-stu-id="8f276-113">Constant</span></span>                                  |
|---------|-------------|-------------------------------------------|
| <span data-ttu-id="8f276-114">64</span><span class="sxs-lookup"><span data-stu-id="8f276-114">64</span></span>      | <span data-ttu-id="8f276-115">0x00000040</span><span class="sxs-lookup"><span data-stu-id="8f276-115">0x00000040</span></span>  | <span data-ttu-id="8f276-116">**msidbDialogAttributesUseCustomPalette**</span><span class="sxs-lookup"><span data-stu-id="8f276-116">**msidbDialogAttributesUseCustomPalette**</span></span> |



 

 

 



