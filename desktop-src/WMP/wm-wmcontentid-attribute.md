---
title: Atributo WM/WMContentID
description: O atributo WM/WMContentID é um GUID que identifica o conteúdo do item.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- Atributo WM/WMContentID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760541"
---
# <a name="wmwmcontentid-attribute"></a><span data-ttu-id="1afb9-104">Atributo WM/WMContentID</span><span class="sxs-lookup"><span data-stu-id="1afb9-104">WM/WMContentID Attribute</span></span>

<span data-ttu-id="1afb9-105">O atributo **WM/WMContentID** é um GUID que identifica o conteúdo do item.</span><span class="sxs-lookup"><span data-stu-id="1afb9-105">The **WM/WMContentID** attribute is a GUID identifying the content of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1afb9-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="1afb9-106">Applies To</span></span>

-   [<span data-ttu-id="1afb9-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="1afb9-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1afb9-108">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="1afb9-108">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="1afb9-109">Atributos de arquivo de mídia do Windows comumente usados</span><span class="sxs-lookup"><span data-stu-id="1afb9-109">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1afb9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="1afb9-110">Remarks</span></span>

<span data-ttu-id="1afb9-111">Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="1afb9-111">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="1afb9-112">**WMContentID** é um alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="1afb9-112">**WMContentID** is an alias for this attribute.</span></span>

<span data-ttu-id="1afb9-113">A constante do Windows Media Format SDK para esse atributo é g \_ wszWMContentID.</span><span class="sxs-lookup"><span data-stu-id="1afb9-113">The Windows Media Format SDK constant for this attribute is g\_wszWMContentID.</span></span>

<span data-ttu-id="1afb9-114">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1afb9-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1afb9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1afb9-115">Requirements</span></span>



| <span data-ttu-id="1afb9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1afb9-116">Requirement</span></span> | <span data-ttu-id="1afb9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1afb9-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1afb9-118">Versão</span><span class="sxs-lookup"><span data-stu-id="1afb9-118">Version</span></span><br/> | <span data-ttu-id="1afb9-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="1afb9-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1afb9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1afb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1afb9-121">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="1afb9-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





