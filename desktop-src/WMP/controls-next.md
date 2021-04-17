---
title: Método Controls. Next
description: O método Next define o item atual para o próximo item na lista de reprodução.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- próximo método Windows Media Player
- próximo método Windows Media Player, classe de controles
- Classe de controles Windows Media Player, próximo método
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58e6d11eafe38b4ab26e0275bd5c986cd4e4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780018"
---
# <a name="controlsnext-method"></a><span data-ttu-id="36f87-106">Método Controls. Next</span><span class="sxs-lookup"><span data-stu-id="36f87-106">Controls.next method</span></span>

<span data-ttu-id="36f87-107">O método **Next** define o item atual para o próximo item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="36f87-107">The **next** method sets the current item to the next item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f87-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36f87-108">Syntax</span></span>


```JScript
Controls.next()
```



## <a name="parameters"></a><span data-ttu-id="36f87-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36f87-109">Parameters</span></span>

<span data-ttu-id="36f87-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="36f87-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36f87-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36f87-111">Return value</span></span>

<span data-ttu-id="36f87-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="36f87-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36f87-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="36f87-113">Remarks</span></span>

<span data-ttu-id="36f87-114">Se a lista de reprodução estiver na última entrada quando o **próximo** for invocado, a primeira entrada da lista de reprodução se tornará a atual.</span><span class="sxs-lookup"><span data-stu-id="36f87-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="36f87-115">Para listas de reprodução do lado do servidor, esse método pula para o próximo item na lista de reprodução do lado do servidor, não a lista de reprodução do cliente.</span><span class="sxs-lookup"><span data-stu-id="36f87-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="36f87-116">Ao reproduzir um DVD, esse método pula para o próximo capítulo lógico na sequência de reprodução, que pode não ser o próximo capítulo da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="36f87-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="36f87-117">Ao reproduzir o DVD ainda, esse método pula para o próximo ainda.</span><span class="sxs-lookup"><span data-stu-id="36f87-117">When playing DVD stills, this method skips to the next still.</span></span>

## <a name="examples"></a><span data-ttu-id="36f87-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36f87-118">Examples</span></span>

<span data-ttu-id="36f87-119">O exemplo a seguir cria um elemento de botão HTML que usa **Next** para mover para o próximo item na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="36f87-119">The following example creates an HTML BUTTON element that uses **next** to move to the next item in the current playlist.</span></span> <span data-ttu-id="36f87-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="36f87-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
">

```



## <a name="requirements"></a><span data-ttu-id="36f87-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f87-121">Requirements</span></span>



| <span data-ttu-id="36f87-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f87-122">Requirement</span></span> | <span data-ttu-id="36f87-123">Valor</span><span class="sxs-lookup"><span data-stu-id="36f87-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36f87-124">Versão</span><span class="sxs-lookup"><span data-stu-id="36f87-124">Version</span></span><br/> | <span data-ttu-id="36f87-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="36f87-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="36f87-126">DLL</span><span class="sxs-lookup"><span data-stu-id="36f87-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="36f87-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36f87-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f87-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="36f87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f87-129">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="36f87-129">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="36f87-130">**Controles. Previous**</span><span class="sxs-lookup"><span data-stu-id="36f87-130">**Controls.previous**</span></span>](controls-previous.md)
</dt> <dt>

[<span data-ttu-id="36f87-131">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="36f87-131">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





