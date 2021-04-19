---
title: Player. playerApplication
description: A propriedade playerApplication recupera o objeto PlayerApplication quando um controle remoto do Windows Media Player está em execução.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player. playerApplication Windows Media Player
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807316"
---
# <a name="playerplayerapplication"></a><span data-ttu-id="eb898-104">Player. playerApplication</span><span class="sxs-lookup"><span data-stu-id="eb898-104">Player.playerApplication</span></span>

<span data-ttu-id="eb898-105">A propriedade **playerApplication** recupera o objeto **playerApplication** quando um controle remoto do Windows Media Player está em execução.</span><span class="sxs-lookup"><span data-stu-id="eb898-105">The **playerApplication** property retrieves the **PlayerApplication** object when a remoted Windows Media Player control is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb898-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb898-106">Syntax</span></span>

<span data-ttu-id="eb898-107">**playerApplication**</span><span class="sxs-lookup"><span data-stu-id="eb898-107">**playerApplication**</span></span>

## <a name="possible-values"></a><span data-ttu-id="eb898-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="eb898-108">Possible Values</span></span>

<span data-ttu-id="eb898-109">Essa propriedade é um objeto **PlayerApplication** somente leitura ou o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="eb898-109">This property is a read-only **PlayerApplication** object or the null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb898-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb898-110">Remarks</span></span>

<span data-ttu-id="eb898-111">Essa propriedade é usada somente quando você faz a comunicação remota do Windows Media Playercontrol.</span><span class="sxs-lookup"><span data-stu-id="eb898-111">This property is used only when remoting the Windows Media Playercontrol.</span></span> <span data-ttu-id="eb898-112">Se o valor for NULL, o Playercontrol de mídia do Windows não será inserido no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="eb898-112">If the value is null, the Windows Media Playercontrol is not embedded in remote mode.</span></span>

<span data-ttu-id="eb898-113">Essa propriedade só pode ser acessada em código C++ ou em código de script em capas por meio da variável global playerApplication.</span><span class="sxs-lookup"><span data-stu-id="eb898-113">This property is only accessible in C++ code or in script code in skins through the playerApplication global variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb898-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb898-114">Requirements</span></span>



| <span data-ttu-id="eb898-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb898-115">Requirement</span></span> | <span data-ttu-id="eb898-116">Valor</span><span class="sxs-lookup"><span data-stu-id="eb898-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb898-117">Versão</span><span class="sxs-lookup"><span data-stu-id="eb898-117">Version</span></span><br/> | <span data-ttu-id="eb898-118">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="eb898-118">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="eb898-119">DLL</span><span class="sxs-lookup"><span data-stu-id="eb898-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb898-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb898-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb898-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb898-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb898-122">**Atributos globais**</span><span class="sxs-lookup"><span data-stu-id="eb898-122">**Global Attributes**</span></span>](global-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb898-123">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="eb898-123">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="eb898-124">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="eb898-124">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="eb898-125">**Estabelecer comunicação remota do controle do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="eb898-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





