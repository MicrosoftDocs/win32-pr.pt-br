---
title: Atributo CDTrackEnabled
description: O atributo CDTrackEnabled indica se a faixa está habilitada para reprodução.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Atributo CDTrackEnabled Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813373"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="15ca8-104">Atributo CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="15ca8-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="15ca8-105">O atributo **CDTrackEnabled** indica se a faixa está habilitada para reprodução.</span><span class="sxs-lookup"><span data-stu-id="15ca8-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="15ca8-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="15ca8-106">Applies To</span></span>

-   [<span data-ttu-id="15ca8-107">Faixas de CD</span><span class="sxs-lookup"><span data-stu-id="15ca8-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="15ca8-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="15ca8-108">Remarks</span></span>

<span data-ttu-id="15ca8-109">Esse atributo é armazenado somente no cache da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="15ca8-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="15ca8-110">Ao reproduzir um CD no Windows Media Player, o usuário pode selecionar uma faixa e especificar que ela não deve ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="15ca8-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="15ca8-111">Esse valor desse atributo será true se a faixa puder ser reproduzida, ou false se o usuário especificou que a faixa não deve ser reproduzida.</span><span class="sxs-lookup"><span data-stu-id="15ca8-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="15ca8-112">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="15ca8-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ca8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ca8-113">Requirements</span></span>



| <span data-ttu-id="15ca8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ca8-114">Requirement</span></span> | <span data-ttu-id="15ca8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="15ca8-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="15ca8-116">Versão</span><span class="sxs-lookup"><span data-stu-id="15ca8-116">Version</span></span><br/> | <span data-ttu-id="15ca8-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="15ca8-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15ca8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="15ca8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ca8-119">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="15ca8-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





