---
title: Método Controls. Play
description: O método Play faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- método play Windows Media Player
- método play Windows Media Player, classe Controls
- Classe Controls Windows Media Player, método play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761475"
---
# <a name="controlsplay-method"></a><span data-ttu-id="a3b04-106">Método Controls. Play</span><span class="sxs-lookup"><span data-stu-id="a3b04-106">Controls.play method</span></span>

<span data-ttu-id="a3b04-107">O método **Play** faz com que o item de mídia atual inicie a reprodução ou retome a reprodução de um item pausado.</span><span class="sxs-lookup"><span data-stu-id="a3b04-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b04-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3b04-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="a3b04-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3b04-109">Parameters</span></span>

<span data-ttu-id="a3b04-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a3b04-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3b04-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3b04-111">Return value</span></span>

<span data-ttu-id="a3b04-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a3b04-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3b04-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3b04-113">Remarks</span></span>

<span data-ttu-id="a3b04-114">Se esse método for chamado durante o encaminhamento rápido ou o retrocesso, o valor das *configurações*. a **taxa** é definida como 1,0.</span><span class="sxs-lookup"><span data-stu-id="a3b04-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="a3b04-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3b04-115">Examples</span></span>

<span data-ttu-id="a3b04-116">O exemplo a seguir cria um elemento de botão HTML que usa **Play** para reproduzir o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="a3b04-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="a3b04-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a3b04-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="a3b04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3b04-118">Requirements</span></span>



| <span data-ttu-id="a3b04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3b04-119">Requirement</span></span> | <span data-ttu-id="a3b04-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a3b04-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b04-121">Versão</span><span class="sxs-lookup"><span data-stu-id="a3b04-121">Version</span></span><br/> | <span data-ttu-id="a3b04-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a3b04-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a3b04-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a3b04-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3b04-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3b04-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3b04-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3b04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b04-126">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="a3b04-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





