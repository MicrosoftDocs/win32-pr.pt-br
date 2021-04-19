---
title: Evento Player. PlaylistChange
description: O evento PlaylistChange ocorre quando uma lista de reprodução é alterada. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Evento PlaylistChange do Windows Media Player
- Evento PlaylistChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796192"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="a3371-107">Evento Player. PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="a3371-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="a3371-108">O evento **PlaylistChange** ocorre quando uma lista de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="a3371-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3371-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3371-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="a3371-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3371-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3371-111">*7.1*</span><span class="sxs-lookup"><span data-stu-id="a3371-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="a3371-112">Objeto **playlist** que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="a3371-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="a3371-113">*change*</span><span class="sxs-lookup"><span data-stu-id="a3371-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="a3371-114">**Número** (**longo**) indicando o tipo de alteração ocorrida na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a3371-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="a3371-115">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="a3371-115">Contains one of the following values.</span></span>



| <span data-ttu-id="a3371-116">Número</span><span class="sxs-lookup"><span data-stu-id="a3371-116">Number</span></span> | <span data-ttu-id="a3371-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a3371-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="a3371-118">0</span><span class="sxs-lookup"><span data-stu-id="a3371-118">0</span></span>      | <span data-ttu-id="a3371-119">Unknown</span><span class="sxs-lookup"><span data-stu-id="a3371-119">Unknown</span></span>       |
| <span data-ttu-id="a3371-120">1</span><span class="sxs-lookup"><span data-stu-id="a3371-120">1</span></span>      | <span data-ttu-id="a3371-121">Limpar</span><span class="sxs-lookup"><span data-stu-id="a3371-121">Clear</span></span>         |
| <span data-ttu-id="a3371-122">2</span><span class="sxs-lookup"><span data-stu-id="a3371-122">2</span></span>      | <span data-ttu-id="a3371-123">InfoChange</span><span class="sxs-lookup"><span data-stu-id="a3371-123">InfoChange</span></span>    |
| <span data-ttu-id="a3371-124">3</span><span class="sxs-lookup"><span data-stu-id="a3371-124">3</span></span>      | <span data-ttu-id="a3371-125">Mover</span><span class="sxs-lookup"><span data-stu-id="a3371-125">Move</span></span>          |
| <span data-ttu-id="a3371-126">4</span><span class="sxs-lookup"><span data-stu-id="a3371-126">4</span></span>      | <span data-ttu-id="a3371-127">Excluir</span><span class="sxs-lookup"><span data-stu-id="a3371-127">Delete</span></span>        |
| <span data-ttu-id="a3371-128">5</span><span class="sxs-lookup"><span data-stu-id="a3371-128">5</span></span>      | <span data-ttu-id="a3371-129">Inserir</span><span class="sxs-lookup"><span data-stu-id="a3371-129">Insert</span></span>        |
| <span data-ttu-id="a3371-130">6</span><span class="sxs-lookup"><span data-stu-id="a3371-130">6</span></span>      | <span data-ttu-id="a3371-131">Acrescentar</span><span class="sxs-lookup"><span data-stu-id="a3371-131">Append</span></span>        |
| <span data-ttu-id="a3371-132">7</span><span class="sxs-lookup"><span data-stu-id="a3371-132">7</span></span>      | <span data-ttu-id="a3371-133">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="a3371-133">Not supported</span></span> |
| <span data-ttu-id="a3371-134">8</span><span class="sxs-lookup"><span data-stu-id="a3371-134">8</span></span>      | <span data-ttu-id="a3371-135">NameChange</span><span class="sxs-lookup"><span data-stu-id="a3371-135">NameChange</span></span>    |
| <span data-ttu-id="a3371-136">9</span><span class="sxs-lookup"><span data-stu-id="a3371-136">9</span></span>      | <span data-ttu-id="a3371-137">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="a3371-137">Not supported</span></span> |
| <span data-ttu-id="a3371-138">10</span><span class="sxs-lookup"><span data-stu-id="a3371-138">10</span></span>     | <span data-ttu-id="a3371-139">Sort</span><span class="sxs-lookup"><span data-stu-id="a3371-139">Sort</span></span>          |



 

<span data-ttu-id="a3371-140">A constante de enumeração de estilo C pode ser derivada por meio da prefixação do valor de nome com "wmplc".</span><span class="sxs-lookup"><span data-stu-id="a3371-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="a3371-141">Por exemplo, a constante para o estado de movimentação é **wmplcMove**.</span><span class="sxs-lookup"><span data-stu-id="a3371-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3371-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3371-142">Return value</span></span>

<span data-ttu-id="a3371-143">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a3371-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3371-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3371-144">Remarks</span></span>

<span data-ttu-id="a3371-145">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="a3371-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a3371-146">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="a3371-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a3371-147">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="a3371-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3371-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3371-148">Requirements</span></span>



| <span data-ttu-id="a3371-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3371-149">Requirement</span></span> | <span data-ttu-id="a3371-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a3371-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3371-151">Versão</span><span class="sxs-lookup"><span data-stu-id="a3371-151">Version</span></span><br/> | <span data-ttu-id="a3371-152">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a3371-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a3371-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a3371-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="a3371-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3371-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3371-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3371-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3371-156">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="a3371-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





