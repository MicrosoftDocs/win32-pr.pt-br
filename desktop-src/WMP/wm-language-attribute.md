---
title: WM/atributo de linguagem
description: O atributo WM/Language é o idioma do item.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/atributo de linguagem Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786233"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="fe403-104">WM/atributo de linguagem</span><span class="sxs-lookup"><span data-stu-id="fe403-104">WM/Language Attribute</span></span>

<span data-ttu-id="fe403-105">O atributo **WM/Language** é o idioma do item.</span><span class="sxs-lookup"><span data-stu-id="fe403-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="fe403-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="fe403-106">Applies To</span></span>

-   [<span data-ttu-id="fe403-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="fe403-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="fe403-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="fe403-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="fe403-109">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="fe403-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="fe403-110">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="fe403-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="fe403-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe403-111">Remarks</span></span>

<span data-ttu-id="fe403-112">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="fe403-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="fe403-113">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="fe403-113">This attribute may have multiple values.</span></span> <span data-ttu-id="fe403-114">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="fe403-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="fe403-115">**Idioma** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="fe403-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="fe403-116">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMLanguage.</span><span class="sxs-lookup"><span data-stu-id="fe403-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="fe403-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fe403-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe403-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe403-118">Requirements</span></span>



| <span data-ttu-id="fe403-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe403-119">Requirement</span></span> | <span data-ttu-id="fe403-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fe403-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe403-121">Versão</span><span class="sxs-lookup"><span data-stu-id="fe403-121">Version</span></span><br/> | <span data-ttu-id="fe403-122">Windows Media Player 9 Series ou posterior (o item de rádio tem suporte apenas no Windows Media Player 9 Series)</span><span class="sxs-lookup"><span data-stu-id="fe403-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe403-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe403-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe403-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="fe403-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="fe403-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="fe403-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





