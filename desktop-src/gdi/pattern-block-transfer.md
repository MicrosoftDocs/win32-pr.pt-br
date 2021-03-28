---
description: O nome da função PatBlt (uma abreviação para transferência de bloco de padrão) implica que essa função simplesmente Replica o pincel (ou padrão) até que ele preencha um retângulo especificado.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transferência de bloco de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988796"
---
# <a name="pattern-block-transfer"></a><span data-ttu-id="30839-103">Transferência de bloco de padrão</span><span class="sxs-lookup"><span data-stu-id="30839-103">Pattern Block Transfer</span></span>

<span data-ttu-id="30839-104">O nome da função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (uma abreviação para transferência de bloco de padrão) implica que essa função simplesmente Replica o pincel (ou padrão) até que ele preencha um retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="30839-104">The name of the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function (an abbreviation for pattern block transfer) implies that this function simply replicates the brush (or pattern) until it fills a specified rectangle.</span></span> <span data-ttu-id="30839-105">No entanto, a função é realmente muito mais potente.</span><span class="sxs-lookup"><span data-stu-id="30839-105">However, the function is actually much more powerful.</span></span> <span data-ttu-id="30839-106">Antes de replicar o pincel, ele combina os dados de cor para o padrão com os dados de cor dos pixels existentes na exibição do vídeo usando uma operação de rasterização (ROP).</span><span class="sxs-lookup"><span data-stu-id="30839-106">Before replicating the brush, it combines the color data for the pattern with the color data for the existing pixels on the video display by using a raster operation (ROP).</span></span> <span data-ttu-id="30839-107">Um ROP é uma operação bit que é aplicada aos bits de dados de cor para o pincel replicado e os bits de dados de cor para o retângulo de destino no dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="30839-107">An ROP is a bitwise operation that is applied to the bits of color data for the replicated brush and the bits of color data for the target rectangle on the display device.</span></span> <span data-ttu-id="30839-108">Há 256 ROPs; no entanto, a função **PatBlt** reconhece apenas aqueles que exigem um padrão e um destino (não aqueles que exigem uma origem).</span><span class="sxs-lookup"><span data-stu-id="30839-108">There are 256 ROPs; however, the **PatBlt** function recognizes only those that require a pattern and a destination (not those that require a source).</span></span> <span data-ttu-id="30839-109">A tabela a seguir identifica o ROPs mais comum.</span><span class="sxs-lookup"><span data-stu-id="30839-109">The following table identifies the most common ROPs.</span></span>



| <span data-ttu-id="30839-110">ROP</span><span class="sxs-lookup"><span data-stu-id="30839-110">ROP</span></span>       | <span data-ttu-id="30839-111">Description</span><span class="sxs-lookup"><span data-stu-id="30839-111">Description</span></span>                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="30839-112">PATCOPY</span><span class="sxs-lookup"><span data-stu-id="30839-112">PATCOPY</span></span>   | <span data-ttu-id="30839-113">Copia o padrão para o bitmap de destino.</span><span class="sxs-lookup"><span data-stu-id="30839-113">Copies the pattern to the destination bitmap.</span></span>                                       |
| <span data-ttu-id="30839-114">PATINVERT</span><span class="sxs-lookup"><span data-stu-id="30839-114">PATINVERT</span></span> | <span data-ttu-id="30839-115">Combina o bitmap de destino com o padrão usando o operador XOR booliano.</span><span class="sxs-lookup"><span data-stu-id="30839-115">Combines the destination bitmap with the pattern by using the Boolean XOR operator.</span></span> |
| <span data-ttu-id="30839-116">DSTINVERT</span><span class="sxs-lookup"><span data-stu-id="30839-116">DSTINVERT</span></span> | <span data-ttu-id="30839-117">Inverte o bitmap de destino.</span><span class="sxs-lookup"><span data-stu-id="30839-117">Inverts the destination bitmap.</span></span>                                                     |
| <span data-ttu-id="30839-118">ESCURIDÃO</span><span class="sxs-lookup"><span data-stu-id="30839-118">BLACKNESS</span></span> | <span data-ttu-id="30839-119">Transforma toda a saída em zeros binários.</span><span class="sxs-lookup"><span data-stu-id="30839-119">Turns all output to binary zeros.</span></span>                                                   |
| <span data-ttu-id="30839-120">DOCUMENTAÇÃO</span><span class="sxs-lookup"><span data-stu-id="30839-120">WHITENESS</span></span> | <span data-ttu-id="30839-121">Transforma todas as saídas em binários.</span><span class="sxs-lookup"><span data-stu-id="30839-121">Turns all output to binary ones.</span></span>                                                    |



 

<span data-ttu-id="30839-122">Para obter mais informações, consulte [raster Operation codes](raster-operation-codes.md).</span><span class="sxs-lookup"><span data-stu-id="30839-122">For more information, see [Raster Operation Codes](raster-operation-codes.md).</span></span>

 

 



