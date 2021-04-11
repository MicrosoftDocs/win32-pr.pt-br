---
title: Objeto cdrom
description: O objeto cdrom fornece uma maneira de acessar um CD ou DVD em sua unidade.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Objeto de cdrom Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104292987"
---
# <a name="cdrom-object"></a><span data-ttu-id="b732c-104">Objeto cdrom</span><span class="sxs-lookup"><span data-stu-id="b732c-104">Cdrom Object</span></span>

<span data-ttu-id="b732c-105">O objeto **cdrom** fornece uma maneira de acessar um CD ou DVD em sua unidade.</span><span class="sxs-lookup"><span data-stu-id="b732c-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="b732c-106">O objeto **cdrom** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b732c-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="b732c-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b732c-107">Property</span></span>                                   | <span data-ttu-id="b732c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b732c-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b732c-109">driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="b732c-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="b732c-110">Recupera a letra da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="b732c-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="b732c-111">playlist</span><span class="sxs-lookup"><span data-stu-id="b732c-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="b732c-112">Recupera um objeto [playlist](playlist-object.md) que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD.</span><span class="sxs-lookup"><span data-stu-id="b732c-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="b732c-113">O objeto **cdrom** dá suporte ao método a seguir.</span><span class="sxs-lookup"><span data-stu-id="b732c-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="b732c-114">Método</span><span class="sxs-lookup"><span data-stu-id="b732c-114">Method</span></span>                   | <span data-ttu-id="b732c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b732c-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="b732c-116">ejeção</span><span class="sxs-lookup"><span data-stu-id="b732c-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="b732c-117">Ejeta o CD ou DVD da unidade.</span><span class="sxs-lookup"><span data-stu-id="b732c-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="b732c-118">O objeto **cdrom** é acessado por meio do método a seguir.</span><span class="sxs-lookup"><span data-stu-id="b732c-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="b732c-119">Objeto</span><span class="sxs-lookup"><span data-stu-id="b732c-119">Object</span></span>                                        | <span data-ttu-id="b732c-120">Método</span><span class="sxs-lookup"><span data-stu-id="b732c-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="b732c-121">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="b732c-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="b732c-122">item</span><span class="sxs-lookup"><span data-stu-id="b732c-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="b732c-123">Para fins de ilustração, Player. cdromCollection. Item (*índice*) é usado nas seções de sintaxe de referência.</span><span class="sxs-lookup"><span data-stu-id="b732c-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="b732c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b732c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b732c-125">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="b732c-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




