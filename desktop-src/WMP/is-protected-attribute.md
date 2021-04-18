---
title: Is_Protected atributo
description: O \_ atributo is Protected indica se o conteúdo é protegido usando o DRM (gerenciamento de direitos digitais).
ms.assetid: 049d4116-7ba6-49f5-ad54-82a98b79d6bc
keywords:
- Atributo Is_Protected Windows Media Player
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba626e72e139a5373973edea581f0f8462eee32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788156"
---
# <a name="is_protected-attribute"></a><span data-ttu-id="19bd1-104">É \_ atributo protegido</span><span class="sxs-lookup"><span data-stu-id="19bd1-104">Is\_Protected Attribute</span></span>

<span data-ttu-id="19bd1-105">O atributo **is \_ Protected** indica se o conteúdo é protegido usando o DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="19bd1-105">The **Is\_Protected** attribute indicates whether the content is protected using digital rights management (DRM).</span></span>

## <a name="applies-to"></a><span data-ttu-id="19bd1-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="19bd1-106">Applies To</span></span>

-   [<span data-ttu-id="19bd1-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="19bd1-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="19bd1-108">Arquivos de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="19bd1-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="19bd1-109">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="19bd1-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="19bd1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="19bd1-110">Remarks</span></span>

<span data-ttu-id="19bd1-111">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="19bd1-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="19bd1-112">**DigitallySecure** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="19bd1-112">**DigitallySecure** is an alias for this attribute.</span></span>

<span data-ttu-id="19bd1-113">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMProtected.</span><span class="sxs-lookup"><span data-stu-id="19bd1-113">The Windows Media Format SDK constant for this attribute is g\_wszWMProtected.</span></span>

<span data-ttu-id="19bd1-114">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="19bd1-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="19bd1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19bd1-115">Requirements</span></span>



| <span data-ttu-id="19bd1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bd1-116">Requirement</span></span> | <span data-ttu-id="19bd1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="19bd1-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="19bd1-118">Versão</span><span class="sxs-lookup"><span data-stu-id="19bd1-118">Version</span></span><br/> | <span data-ttu-id="19bd1-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="19bd1-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19bd1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="19bd1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19bd1-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="19bd1-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





