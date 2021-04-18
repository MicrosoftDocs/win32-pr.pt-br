---
title: Atributo FileSize
description: O atributo FileSize é o tamanho do arquivo em bytes.
ms.assetid: e845cc82-6975-4fd9-800f-a66f59a5fb39
keywords:
- Atributo FileSize Windows Media Player
topic_type:
- apiref
api_name:
- FileSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee243d85be59502acead3614dced49494c11104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810549"
---
# <a name="filesize-attribute"></a><span data-ttu-id="4a4d0-104">Atributo FileSize</span><span class="sxs-lookup"><span data-stu-id="4a4d0-104">FileSize Attribute</span></span>

<span data-ttu-id="4a4d0-105">O atributo **filesize** é o tamanho do arquivo em bytes.</span><span class="sxs-lookup"><span data-stu-id="4a4d0-105">The **FileSize** attribute is the size of the file in bytes.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4a4d0-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="4a4d0-106">Applies To</span></span>

-   [<span data-ttu-id="4a4d0-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="4a4d0-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="4a4d0-108">Arquivos de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="4a4d0-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="4a4d0-109">Outros itens</span><span class="sxs-lookup"><span data-stu-id="4a4d0-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="4a4d0-110">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="4a4d0-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="4a4d0-111">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="4a4d0-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="4a4d0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a4d0-112">Remarks</span></span>

<span data-ttu-id="4a4d0-113">Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="4a4d0-113">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="4a4d0-114">**Size** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="4a4d0-114">**Size** is an alias for this attribute.</span></span>

<span data-ttu-id="4a4d0-115">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMFileSize.</span><span class="sxs-lookup"><span data-stu-id="4a4d0-115">The Windows Media Format SDK constant for this attribute is g\_wszWMFileSize.</span></span>

<span data-ttu-id="4a4d0-116">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4a4d0-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a4d0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a4d0-117">Requirements</span></span>



| <span data-ttu-id="4a4d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a4d0-118">Requirement</span></span> | <span data-ttu-id="4a4d0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4a4d0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a4d0-120">Versão</span><span class="sxs-lookup"><span data-stu-id="4a4d0-120">Version</span></span><br/> | <span data-ttu-id="4a4d0-121">Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)</span><span class="sxs-lookup"><span data-stu-id="4a4d0-121">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a4d0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a4d0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a4d0-123">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="4a4d0-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





