---
title: Objeto PlayerApplication
description: O objeto PlayerApplication fornece uma maneira de coordenar a alternância entre um controle do Windows Media Player remoto e o modo completo do Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objeto PlayerApplication Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293427"
---
# <a name="playerapplication-object"></a><span data-ttu-id="b7bf5-104">Objeto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="b7bf5-104">PlayerApplication Object</span></span>

<span data-ttu-id="b7bf5-105">O objeto **PlayerApplication** fornece uma maneira de coordenar a alternância entre um controle do Windows Media Player remoto e o modo completo do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="b7bf5-106">Esse objeto é usado somente com programas C++ que implementam a interface **IWMPRemoteMediaServices** e inserem o controle Player no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="b7bf5-107">Arquivos de capa usados como interfaces personalizadas para o controle remoto do Windows Media Player acessam esse objeto no código de script por meio do atributo global **playerApplication** .</span><span class="sxs-lookup"><span data-stu-id="b7bf5-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="b7bf5-108">O objeto **PlayerApplication** dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="b7bf5-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b7bf5-109">Property</span></span>                                           | <span data-ttu-id="b7bf5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7bf5-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7bf5-111">hasDisplay</span><span class="sxs-lookup"><span data-stu-id="b7bf5-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="b7bf5-112">Recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="b7bf5-113">playerDocked</span><span class="sxs-lookup"><span data-stu-id="b7bf5-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="b7bf5-114">Recupera um valor que indica se o Windows Media Player está em um estado encaixado.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="b7bf5-115">O objeto **PlayerApplication** dá suporte aos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="b7bf5-116">Método</span><span class="sxs-lookup"><span data-stu-id="b7bf5-116">Method</span></span>                                                                       | <span data-ttu-id="b7bf5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7bf5-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="b7bf5-118">switchToControl</span><span class="sxs-lookup"><span data-stu-id="b7bf5-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="b7bf5-119">Alterna um controle do Windows Media Player remoto para o estado encaixado.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="b7bf5-120">switchToPlayerApplication</span><span class="sxs-lookup"><span data-stu-id="b7bf5-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="b7bf5-121">Alterna um controle remoto do Windows Media Player para o modo completo do Player.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="b7bf5-122">O objeto **PlayerApplication** é acessado por meio da propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="b7bf5-123">Objeto</span><span class="sxs-lookup"><span data-stu-id="b7bf5-123">Object</span></span>                      | <span data-ttu-id="b7bf5-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b7bf5-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="b7bf5-125">Jogador</span><span class="sxs-lookup"><span data-stu-id="b7bf5-125">Player</span></span>](player-object.md) | [<span data-ttu-id="b7bf5-126">playerApplication</span><span class="sxs-lookup"><span data-stu-id="b7bf5-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="b7bf5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7bf5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bf5-128">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="b7bf5-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="b7bf5-129">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="b7bf5-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




