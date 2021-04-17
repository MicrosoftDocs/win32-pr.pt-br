---
title: Atributo do WM/year
description: O atributo WM/year é o ano em que o conteúdo foi publicado.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- Atributo do WM/year do Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749552"
---
# <a name="wmyear-attribute"></a><span data-ttu-id="6efea-104">Atributo do WM/year</span><span class="sxs-lookup"><span data-stu-id="6efea-104">WM/Year Attribute</span></span>

<span data-ttu-id="6efea-105">O atributo **WM/year** é o ano em que o conteúdo foi publicado.</span><span class="sxs-lookup"><span data-stu-id="6efea-105">The **WM/Year** attribute is the year the content was published.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6efea-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="6efea-106">Applies To</span></span>

-   [<span data-ttu-id="6efea-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="6efea-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6efea-108">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="6efea-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6efea-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6efea-109">Remarks</span></span>

<span data-ttu-id="6efea-110">Esse atributo é armazenado somente no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="6efea-110">This attribute is stored only in the digital media file.</span></span>

<span data-ttu-id="6efea-111">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6efea-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

<span data-ttu-id="6efea-112">Esse atributo não deve ser usado como parte de uma condição de consulta.</span><span class="sxs-lookup"><span data-stu-id="6efea-112">This attribute should not be used as part of a query condition.</span></span> <span data-ttu-id="6efea-113">Ele é derivado de outro atributo e não pode ser consultado diretamente em uma coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="6efea-113">It is derived from another attribute and cannot be directly queried against in a media collection.</span></span>

<span data-ttu-id="6efea-114">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMYear.</span><span class="sxs-lookup"><span data-stu-id="6efea-114">The Windows Media Format SDK constant for this attribute is g\_wszWMYear.</span></span>

## <a name="requirements"></a><span data-ttu-id="6efea-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6efea-115">Requirements</span></span>



| <span data-ttu-id="6efea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6efea-116">Requirement</span></span> | <span data-ttu-id="6efea-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6efea-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6efea-118">Versão</span><span class="sxs-lookup"><span data-stu-id="6efea-118">Version</span></span><br/> | <span data-ttu-id="6efea-119">O Windows Media Player 9 Series Windows Media Player 10 ou posterior não oferece suporte a esse atributo</span><span class="sxs-lookup"><span data-stu-id="6efea-119">Windows Media Player 9 Series Windows Media Player 10 or later does not support this attribute</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6efea-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6efea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efea-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="6efea-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





