---
title: Atributo de descrição (SDK do WMP)
description: O atributo de descrição é uma descrição do conteúdo.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Atributo de descrição Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762086"
---
# <a name="description-attribute"></a><span data-ttu-id="c10bb-104">Atributo de descrição</span><span class="sxs-lookup"><span data-stu-id="c10bb-104">Description Attribute</span></span>

<span data-ttu-id="c10bb-105">O atributo de **Descrição** é uma descrição do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c10bb-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c10bb-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="c10bb-106">Applies To</span></span>

-   [<span data-ttu-id="c10bb-107">Arquivos de música</span><span class="sxs-lookup"><span data-stu-id="c10bb-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c10bb-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="c10bb-108">Remarks</span></span>

<span data-ttu-id="c10bb-109">Esse atributo é armazenado em arquivos de música, não na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="c10bb-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="c10bb-110">Esse atributo pode ter vários valores.</span><span class="sxs-lookup"><span data-stu-id="c10bb-110">This attribute may have multiple values.</span></span> <span data-ttu-id="c10bb-111">Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar a *mídia*. método **getItemInfoByType** , não o método *Media*. getItemInfo.</span><span class="sxs-lookup"><span data-stu-id="c10bb-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="c10bb-112">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMDescription.</span><span class="sxs-lookup"><span data-stu-id="c10bb-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="c10bb-113">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c10bb-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c10bb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c10bb-114">Requirements</span></span>



| <span data-ttu-id="c10bb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10bb-115">Requirement</span></span> | <span data-ttu-id="c10bb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c10bb-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c10bb-117">Versão</span><span class="sxs-lookup"><span data-stu-id="c10bb-117">Version</span></span><br/> | <span data-ttu-id="c10bb-118">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c10bb-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c10bb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c10bb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c10bb-120">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="c10bb-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





