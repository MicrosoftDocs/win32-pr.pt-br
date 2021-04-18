---
title: Atributo SyncOnly
description: O atributo SyncOnly é uma representação de cadeia de caracteres de um valor booliano que o Windows Media Player usa para determinar se uma lista de reprodução está disponível apenas para sincronização.
ms.assetid: 36149bb9-3a0b-4f6d-8be3-97d2a87faa83
keywords:
- Atributo SyncOnly Windows Media Player
topic_type:
- apiref
api_name:
- SyncOnly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0245ffac2c4c64717adf669fcc6ff8fd0768382
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780334"
---
# <a name="synconly-attribute"></a><span data-ttu-id="a5484-104">Atributo SyncOnly</span><span class="sxs-lookup"><span data-stu-id="a5484-104">SyncOnly Attribute</span></span>

<span data-ttu-id="a5484-105">O atributo **SyncOnly** é uma representação de cadeia de caracteres de um valor **booliano** que o Windows Media Player usa para determinar se uma lista de reprodução está disponível apenas para sincronização.</span><span class="sxs-lookup"><span data-stu-id="a5484-105">The **SyncOnly** attribute is a string representation of a **Boolean** value that Windows Media Player uses to determine whether a playlist is available only for synchronization.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a5484-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="a5484-106">Applies To</span></span>

-   [<span data-ttu-id="a5484-107">Playlists</span><span class="sxs-lookup"><span data-stu-id="a5484-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="a5484-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5484-108">Remarks</span></span>

<span data-ttu-id="a5484-109">Um valor de 1 indica que a playlist está disponível somente para sincronização e não pode aparecer no nó de **playlist automática** .</span><span class="sxs-lookup"><span data-stu-id="a5484-109">A value of 1 indicates that the playlist is available only for synchronization and cannot appear in the **Auto Playlist** node.</span></span> <span data-ttu-id="a5484-110">Um valor de zero indica que a lista de reprodução pode aparecer no nó de **playlist automática** .</span><span class="sxs-lookup"><span data-stu-id="a5484-110">A value of zero indicates that the playlist can appear in the **Auto Playlist** node.</span></span>

<span data-ttu-id="a5484-111">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="a5484-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5484-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5484-112">Requirements</span></span>



| <span data-ttu-id="a5484-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5484-113">Requirement</span></span> | <span data-ttu-id="a5484-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a5484-114">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="a5484-115">Versão</span><span class="sxs-lookup"><span data-stu-id="a5484-115">Version</span></span><br/> | <span data-ttu-id="a5484-116">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a5484-116">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5484-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5484-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5484-118">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="a5484-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





