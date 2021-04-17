---
title: Atributo AverageLevel
description: O atributo AverageLevel é um valor de amplitude de 16 bits que indica o nível médio de volume.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Atributo AverageLevel Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760897"
---
# <a name="averagelevel-attribute"></a><span data-ttu-id="5cc4c-104">Atributo AverageLevel</span><span class="sxs-lookup"><span data-stu-id="5cc4c-104">AverageLevel Attribute</span></span>

<span data-ttu-id="5cc4c-105">O atributo **AverageLevel** é um valor de amplitude de 16 bits que indica o nível médio de volume.</span><span class="sxs-lookup"><span data-stu-id="5cc4c-105">The **AverageLevel** attribute is a 16-bit amplitude value indicating the average volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5cc4c-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="5cc4c-106">Applies To</span></span>

-   [<span data-ttu-id="5cc4c-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="5cc4c-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5cc4c-108">Arquivos de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="5cc4c-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5cc4c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cc4c-109">Remarks</span></span>

<span data-ttu-id="5cc4c-110">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="5cc4c-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="5cc4c-111">O Windows Media Player define esse valor em uma das seguintes instâncias:</span><span class="sxs-lookup"><span data-stu-id="5cc4c-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="5cc4c-112">Depois de copiar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cc4c-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="5cc4c-113">Depois de reproduzir um arquivo (quando o aprimoramento do nivelamento de volume automático estiver habilitado).</span><span class="sxs-lookup"><span data-stu-id="5cc4c-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="5cc4c-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszAverageLevel.</span><span class="sxs-lookup"><span data-stu-id="5cc4c-114">The Windows Media Format SDK constant for this attribute is g\_wszAverageLevel.</span></span>

<span data-ttu-id="5cc4c-115">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5cc4c-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cc4c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc4c-116">Requirements</span></span>



| <span data-ttu-id="5cc4c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cc4c-117">Requirement</span></span> | <span data-ttu-id="5cc4c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5cc4c-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="5cc4c-119">Versão</span><span class="sxs-lookup"><span data-stu-id="5cc4c-119">Version</span></span><br/> | <span data-ttu-id="5cc4c-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5cc4c-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cc4c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cc4c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc4c-122">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="5cc4c-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





