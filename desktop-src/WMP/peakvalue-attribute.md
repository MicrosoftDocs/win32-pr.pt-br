---
title: Atributo de picovalue
description: O atributo de Picovalue é um valor de amplitude de 16 bits que indica o nível de volume de pico.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Atributo de picovalue Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763833"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="c2c5d-104">Atributo de picovalue</span><span class="sxs-lookup"><span data-stu-id="c2c5d-104">PeakValue Attribute</span></span>

<span data-ttu-id="c2c5d-105">O atributo de **picovalue** é um valor de amplitude de 16 bits que indica o nível de volume de pico.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c2c5d-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="c2c5d-106">Applies To</span></span>

-   [<span data-ttu-id="c2c5d-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="c2c5d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="c2c5d-108">Arquivos de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="c2c5d-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c2c5d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2c5d-109">Remarks</span></span>

<span data-ttu-id="c2c5d-110">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="c2c5d-111">O Windows Media Player define esse valor em uma das seguintes instâncias:</span><span class="sxs-lookup"><span data-stu-id="c2c5d-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="c2c5d-112">Depois de copiar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="c2c5d-113">Depois de reproduzir um arquivo (quando o aprimoramento do nivelamento de volume automático estiver habilitado).</span><span class="sxs-lookup"><span data-stu-id="c2c5d-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="c2c5d-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszPeakValue.</span><span class="sxs-lookup"><span data-stu-id="c2c5d-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="c2c5d-115">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c2c5d-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c5d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2c5d-116">Requirements</span></span>



| <span data-ttu-id="c2c5d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2c5d-117">Requirement</span></span> | <span data-ttu-id="c2c5d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c2c5d-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c2c5d-119">Versão</span><span class="sxs-lookup"><span data-stu-id="c2c5d-119">Version</span></span><br/> | <span data-ttu-id="c2c5d-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c2c5d-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2c5d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2c5d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c5d-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="c2c5d-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





