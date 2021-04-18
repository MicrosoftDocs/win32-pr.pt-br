---
title: Settings. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | Settings. IsAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Settings. isdisponível Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752590"
---
# <a name="settingsisavailable"></a><span data-ttu-id="e64b9-105">Settings. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="e64b9-105">Settings.isAvailable</span></span>

<span data-ttu-id="e64b9-106">A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="e64b9-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e64b9-107">Syntax</span></span>

<span data-ttu-id="e64b9-108">Player. Settings. IsAvailable (nome)</span><span class="sxs-lookup"><span data-stu-id="e64b9-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="e64b9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e64b9-109">Parameters</span></span>

<span data-ttu-id="e64b9-110">*name*</span><span class="sxs-lookup"><span data-stu-id="e64b9-110">*name*</span></span>

<span data-ttu-id="e64b9-111">Cadeia de caracteres que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e64b9-111">String containing one of the following values.</span></span>



| <span data-ttu-id="e64b9-112">String</span><span class="sxs-lookup"><span data-stu-id="e64b9-112">String</span></span>             | <span data-ttu-id="e64b9-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e64b9-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="e64b9-114">AutoStart</span><span class="sxs-lookup"><span data-stu-id="e64b9-114">AutoStart</span></span>          | <span data-ttu-id="e64b9-115">Determina se a propriedade AutoStart pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="e64b9-116">Saldo</span><span class="sxs-lookup"><span data-stu-id="e64b9-116">Balance</span></span>            | <span data-ttu-id="e64b9-117">Determina se a propriedade de saldo pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="e64b9-118">BaseURL</span><span class="sxs-lookup"><span data-stu-id="e64b9-118">BaseURL</span></span>            | <span data-ttu-id="e64b9-119">Determina se a propriedade baseURL pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="e64b9-120">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="e64b9-120">DefaultFrame</span></span>       | <span data-ttu-id="e64b9-121">Determina se a propriedade DefaultFrame pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="e64b9-122">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="e64b9-122">EnableErrorDialogs</span></span> | <span data-ttu-id="e64b9-123">Determina se a propriedade enableErrorDialogs pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="e64b9-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="e64b9-124">GetMode</span></span>            | <span data-ttu-id="e64b9-125">Determina se o método GetMode pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="e64b9-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="e64b9-126">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="e64b9-126">InvokeURLs</span></span>         | <span data-ttu-id="e64b9-127">Determina se a propriedade invokeURLs pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="e64b9-128">Mute</span><span class="sxs-lookup"><span data-stu-id="e64b9-128">Mute</span></span>               | <span data-ttu-id="e64b9-129">Determina se a propriedade de mudo pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="e64b9-130">PlayCount</span><span class="sxs-lookup"><span data-stu-id="e64b9-130">PlayCount</span></span>          | <span data-ttu-id="e64b9-131">Determina se a propriedade playCount pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="e64b9-132">Tarifa</span><span class="sxs-lookup"><span data-stu-id="e64b9-132">Rate</span></span>               | <span data-ttu-id="e64b9-133">Determina se a propriedade de taxa pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="e64b9-134">Setmode</span><span class="sxs-lookup"><span data-stu-id="e64b9-134">SetMode</span></span>            | <span data-ttu-id="e64b9-135">Determina se o método setmode pode ser chamado.</span><span class="sxs-lookup"><span data-stu-id="e64b9-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="e64b9-136">Volume</span><span class="sxs-lookup"><span data-stu-id="e64b9-136">Volume</span></span>             | <span data-ttu-id="e64b9-137">Determina se a propriedade do volume pode ser definida.</span><span class="sxs-lookup"><span data-stu-id="e64b9-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="e64b9-138">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e64b9-138">Return Values</span></span>

<span data-ttu-id="e64b9-139">Esse método retorna um valor **booliano** .</span><span class="sxs-lookup"><span data-stu-id="e64b9-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e64b9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e64b9-140">Requirements</span></span>



| <span data-ttu-id="e64b9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64b9-141">Requirement</span></span> | <span data-ttu-id="e64b9-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e64b9-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e64b9-143">Versão</span><span class="sxs-lookup"><span data-stu-id="e64b9-143">Version</span></span><br/> | <span data-ttu-id="e64b9-144">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e64b9-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e64b9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e64b9-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="e64b9-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64b9-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e64b9-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e64b9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64b9-148">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="e64b9-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





