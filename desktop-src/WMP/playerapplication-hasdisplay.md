---
title: PlayerApplication.hasDisplay
description: A propriedade hasDisplay recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Player remoto.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- PlayerApplication. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814019"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="6bca3-104">PlayerApplication.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="6bca3-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="6bca3-105">A propriedade **hasDisplay** recupera um valor que indica se o vídeo pode ser exibido por meio do controle de Player remoto.</span><span class="sxs-lookup"><span data-stu-id="6bca3-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bca3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bca3-106">Syntax</span></span>

<span data-ttu-id="6bca3-107">*playerApplication*. **hasDisplay**</span><span class="sxs-lookup"><span data-stu-id="6bca3-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6bca3-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="6bca3-108">Possible Values</span></span>

<span data-ttu-id="6bca3-109">Esta propriedade é um **booliano** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6bca3-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bca3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bca3-110">Remarks</span></span>

<span data-ttu-id="6bca3-111">Essa propriedade é usada somente quando você faz a comunicação remota do controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6bca3-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="6bca3-112">Vários controles do Windows Media Player podem ser executados remotamente ao mesmo tempo, mas o vídeo só pode ser exibido em um local de cada vez, seja no modo completo do Player ou em um dos controles remotos do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6bca3-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="6bca3-113">Use essa propriedade para determinar se o controle atual é aquele pelo qual o vídeo pode ser exibido.</span><span class="sxs-lookup"><span data-stu-id="6bca3-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="6bca3-114">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="6bca3-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bca3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bca3-115">Requirements</span></span>



| <span data-ttu-id="6bca3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bca3-116">Requirement</span></span> | <span data-ttu-id="6bca3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6bca3-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bca3-118">Versão</span><span class="sxs-lookup"><span data-stu-id="6bca3-118">Version</span></span><br/> | <span data-ttu-id="6bca3-119">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="6bca3-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6bca3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6bca3-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bca3-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bca3-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bca3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bca3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bca3-123">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="6bca3-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="6bca3-124">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="6bca3-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





