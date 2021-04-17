---
title: Atributo do WM/Writer
description: O atributo WM/Writer é o nome do gravador que escreveu as palavras do conteúdo.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Atributo do WM/Writer do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748890"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="75056-104">Atributo do WM/Writer</span><span class="sxs-lookup"><span data-stu-id="75056-104">WM/Writer Attribute</span></span>

<span data-ttu-id="75056-105">O atributo **WM/Writer** é o nome do gravador que escreveu as palavras do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="75056-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="75056-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="75056-106">Applies To</span></span>

-   [<span data-ttu-id="75056-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="75056-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="75056-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="75056-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="75056-109">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="75056-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="75056-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="75056-110">Remarks</span></span>

<span data-ttu-id="75056-111">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="75056-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="75056-112">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="75056-112">This attribute may have multiple values.</span></span> <span data-ttu-id="75056-113">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="75056-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="75056-114">O **gravador** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="75056-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="75056-115">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMWriter.</span><span class="sxs-lookup"><span data-stu-id="75056-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="75056-116">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="75056-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="75056-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75056-117">Requirements</span></span>



| <span data-ttu-id="75056-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75056-118">Requirement</span></span> | <span data-ttu-id="75056-119">Valor</span><span class="sxs-lookup"><span data-stu-id="75056-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="75056-120">Versão</span><span class="sxs-lookup"><span data-stu-id="75056-120">Version</span></span><br/> | <span data-ttu-id="75056-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="75056-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75056-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="75056-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75056-123">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="75056-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="75056-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="75056-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





