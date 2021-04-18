---
title: Método Controls. Previous
description: O método anterior define o item atual para o item anterior na lista de reprodução.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- método anterior Windows Media Player
- método anterior Windows Media Player, classe Controls
- Classe Controls do Windows Media Player, método anterior
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760270"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="e3453-106">Método Controls. Previous</span><span class="sxs-lookup"><span data-stu-id="e3453-106">Controls.previous method</span></span>

<span data-ttu-id="e3453-107">O método **anterior** define o item atual para o item anterior na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e3453-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3453-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3453-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="e3453-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3453-109">Parameters</span></span>

<span data-ttu-id="e3453-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e3453-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3453-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3453-111">Return value</span></span>

<span data-ttu-id="e3453-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e3453-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3453-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3453-113">Remarks</span></span>

<span data-ttu-id="e3453-114">Se a lista de reprodução estiver na primeira entrada quando a **anterior** for invocada, a última entrada na lista de reprodução se tornará a atual.</span><span class="sxs-lookup"><span data-stu-id="e3453-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="e3453-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3453-115">Examples</span></span>

<span data-ttu-id="e3453-116">O exemplo a seguir cria um elemento de botão HTML que usa **Previous** para mover para o item anterior na playlist atual.</span><span class="sxs-lookup"><span data-stu-id="e3453-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="e3453-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e3453-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="e3453-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3453-118">Requirements</span></span>



| <span data-ttu-id="e3453-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3453-119">Requirement</span></span> | <span data-ttu-id="e3453-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3453-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3453-121">Versão</span><span class="sxs-lookup"><span data-stu-id="e3453-121">Version</span></span><br/> | <span data-ttu-id="e3453-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e3453-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e3453-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e3453-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3453-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3453-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3453-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3453-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3453-126">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="e3453-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="e3453-127">**Controles. Next**</span><span class="sxs-lookup"><span data-stu-id="e3453-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="e3453-128">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="e3453-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





