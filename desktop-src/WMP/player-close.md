---
title: Método Player. Close
description: O método Close libera recursos do Windows Media Player.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- fechar o método Windows Media Player
- método Close Windows Media Player, classe Player
- Classe de jogador Windows Media Player, método Close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790482"
---
# <a name="playerclose-method"></a><span data-ttu-id="50f97-106">Método Player. Close</span><span class="sxs-lookup"><span data-stu-id="50f97-106">Player.close method</span></span>

<span data-ttu-id="50f97-107">O método **Close** libera recursos do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="50f97-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="50f97-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50f97-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="50f97-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50f97-109">Parameters</span></span>

<span data-ttu-id="50f97-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="50f97-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50f97-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50f97-111">Return value</span></span>

<span data-ttu-id="50f97-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="50f97-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f97-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="50f97-113">Remarks</span></span>

<span data-ttu-id="50f97-114">Esse método fecha o arquivo de mídia digital atual, não o Windows Media Player em si.</span><span class="sxs-lookup"><span data-stu-id="50f97-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="50f97-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="50f97-115">Examples</span></span>

<span data-ttu-id="50f97-116">O exemplo a seguir cria um elemento de botão HTML que, quando clicado, interrompe a reprodução no Windows Media Player e libera os recursos em uso.</span><span class="sxs-lookup"><span data-stu-id="50f97-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="50f97-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="50f97-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="50f97-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50f97-118">Requirements</span></span>



| <span data-ttu-id="50f97-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50f97-119">Requirement</span></span> | <span data-ttu-id="50f97-120">Valor</span><span class="sxs-lookup"><span data-stu-id="50f97-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50f97-121">Versão</span><span class="sxs-lookup"><span data-stu-id="50f97-121">Version</span></span><br/> | <span data-ttu-id="50f97-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="50f97-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="50f97-123">DLL</span><span class="sxs-lookup"><span data-stu-id="50f97-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="50f97-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50f97-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f97-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="50f97-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50f97-126">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="50f97-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





