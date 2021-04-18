---
title: Atributo PLAYERAPPLICATION. hasDisplay
description: O atributo hasDisplay recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786143"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="c1703-104">PLAYERAPPLICATION.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="c1703-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="c1703-105">O atributo **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle remoto do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c1703-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="c1703-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c1703-106">Possible Values</span></span>

<span data-ttu-id="c1703-107">Esse atributo é um **booliano** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c1703-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="c1703-108">Valor</span><span class="sxs-lookup"><span data-stu-id="c1703-108">Value</span></span> | <span data-ttu-id="c1703-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1703-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="c1703-110">True</span><span class="sxs-lookup"><span data-stu-id="c1703-110">True</span></span>  | <span data-ttu-id="c1703-111">O vídeo pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c1703-111">The video can display.</span></span>    |
| <span data-ttu-id="c1703-112">Falso</span><span class="sxs-lookup"><span data-stu-id="c1703-112">False</span></span> | <span data-ttu-id="c1703-113">O vídeo não pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c1703-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c1703-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1703-114">Remarks</span></span>

<span data-ttu-id="c1703-115">Esse atributo é usado somente quando você faz a comunicação remota do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c1703-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="c1703-116">Vários controles do Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local de cada vez, seja no modo completo do Player ou em um dos controles remotos.</span><span class="sxs-lookup"><span data-stu-id="c1703-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="c1703-117">Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c1703-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1703-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1703-118">Requirements</span></span>



| <span data-ttu-id="c1703-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1703-119">Requirement</span></span> | <span data-ttu-id="c1703-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c1703-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="c1703-121">Versão</span><span class="sxs-lookup"><span data-stu-id="c1703-121">Version</span></span><br/> | <span data-ttu-id="c1703-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c1703-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1703-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1703-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1703-124">**Elemento PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="c1703-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="c1703-125">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c1703-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





