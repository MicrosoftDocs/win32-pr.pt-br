---
title: Atributo temporário
description: O atributo temporário especifica se uma playlist é temporária.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Atributo temporário Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811948"
---
# <a name="temporary-attribute"></a><span data-ttu-id="34f66-104">Atributo temporário</span><span class="sxs-lookup"><span data-stu-id="34f66-104">Temporary Attribute</span></span>

<span data-ttu-id="34f66-105">O atributo **temporário** especifica se uma playlist é temporária.</span><span class="sxs-lookup"><span data-stu-id="34f66-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="34f66-106">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="34f66-106">**Remarks**</span></span>

<span data-ttu-id="34f66-107">Se você tiver recuperado uma lista de reprodução da biblioteca, as alterações feitas na playlist serão refletidas na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="34f66-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="34f66-108">Para evitar isso, chame [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passando o nome do atributo "Temporary" e o valor "true".</span><span class="sxs-lookup"><span data-stu-id="34f66-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="34f66-109">Isso converte a instância de playlist em uma playlist temporária, que é segura para ser editada sem alterar a playlist original.</span><span class="sxs-lookup"><span data-stu-id="34f66-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="34f66-110">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="34f66-110">**Applies To**</span></span>

-   [<span data-ttu-id="34f66-111">Playlists</span><span class="sxs-lookup"><span data-stu-id="34f66-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="34f66-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34f66-112">Requirements</span></span>



| <span data-ttu-id="34f66-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="34f66-113">Requirement</span></span> | <span data-ttu-id="34f66-114">Valor</span><span class="sxs-lookup"><span data-stu-id="34f66-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="34f66-115">Versão</span><span class="sxs-lookup"><span data-stu-id="34f66-115">Version</span></span><br/> | <span data-ttu-id="34f66-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="34f66-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34f66-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="34f66-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f66-118">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="34f66-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





