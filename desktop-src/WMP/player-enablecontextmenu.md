---
title: Player. enableContextMenu
description: A propriedade enableContextMenu especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enableContextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785004"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="40049-104">Player. enableContextMenu</span><span class="sxs-lookup"><span data-stu-id="40049-104">Player.enableContextMenu</span></span>

<span data-ttu-id="40049-105">A propriedade **enableContextMenu** especifica ou recupera um valor que indica se o menu de contexto deve ser habilitado, que aparece quando o botão direito do mouse é clicado.</span><span class="sxs-lookup"><span data-stu-id="40049-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="40049-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="40049-106">Syntax</span></span>

<span data-ttu-id="40049-107">*Player*. **enableContextMenu**</span><span class="sxs-lookup"><span data-stu-id="40049-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="40049-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="40049-108">Possible Values</span></span>

<span data-ttu-id="40049-109">Esta propriedade é um booliano de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="40049-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="40049-110">Valor</span><span class="sxs-lookup"><span data-stu-id="40049-110">Value</span></span> | <span data-ttu-id="40049-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="40049-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="40049-112">true</span><span class="sxs-lookup"><span data-stu-id="40049-112">true</span></span>  | <span data-ttu-id="40049-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="40049-113">Default.</span></span> <span data-ttu-id="40049-114">Habilite o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="40049-114">Enable the context menu.</span></span> |
| <span data-ttu-id="40049-115">false</span><span class="sxs-lookup"><span data-stu-id="40049-115">false</span></span> | <span data-ttu-id="40049-116">Não habilite o menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="40049-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="40049-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="40049-117">Remarks</span></span>

<span data-ttu-id="40049-118">Durante a reprodução de tela inteira, o Windows Media Player oculta o cursor do mouse quando **enableContextMenu** é igual a false e **UIMODE** é igual a "None".</span><span class="sxs-lookup"><span data-stu-id="40049-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="40049-119">**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="40049-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="40049-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40049-120">Requirements</span></span>



| <span data-ttu-id="40049-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="40049-121">Requirement</span></span> | <span data-ttu-id="40049-122">Valor</span><span class="sxs-lookup"><span data-stu-id="40049-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40049-123">Versão</span><span class="sxs-lookup"><span data-stu-id="40049-123">Version</span></span><br/> | <span data-ttu-id="40049-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="40049-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="40049-125">DLL</span><span class="sxs-lookup"><span data-stu-id="40049-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="40049-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40049-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40049-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="40049-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40049-128">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="40049-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





