---
title: Método Settings. setmode
description: O método setmode define vários modos como ativo ou inativo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- método setmode do Windows Media Player
- método setmode Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método setmode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747495"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="3b464-106">Método Settings. setmode</span><span class="sxs-lookup"><span data-stu-id="3b464-106">Settings.setMode method</span></span>

<span data-ttu-id="3b464-107">O método **setmode** define vários modos como ativo ou inativo.</span><span class="sxs-lookup"><span data-stu-id="3b464-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b464-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b464-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="3b464-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b464-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b464-110">*modeName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b464-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b464-111">**Cadeia de caracteres** que especifica o nome do modo que está sendo alterado, contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b464-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="3b464-112">String</span><span class="sxs-lookup"><span data-stu-id="3b464-112">String</span></span>     | <span data-ttu-id="3b464-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b464-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b464-114">rebobinar</span><span class="sxs-lookup"><span data-stu-id="3b464-114">autoRewind</span></span> | <span data-ttu-id="3b464-115">Modo que indica se as faixas são rebobinadas para o início após a reprodução até o fim.</span><span class="sxs-lookup"><span data-stu-id="3b464-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="3b464-116">O estado padrão é true.</span><span class="sxs-lookup"><span data-stu-id="3b464-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="3b464-117">loop</span><span class="sxs-lookup"><span data-stu-id="3b464-117">loop</span></span>       | <span data-ttu-id="3b464-118">Modo que indica se a sequência de faixas se repete.</span><span class="sxs-lookup"><span data-stu-id="3b464-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="3b464-119">O estado padrão é false.</span><span class="sxs-lookup"><span data-stu-id="3b464-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="3b464-120">conmoldura</span><span class="sxs-lookup"><span data-stu-id="3b464-120">showFrame</span></span>  | <span data-ttu-id="3b464-121">Modo que indica se o quadro de chave de vídeo mais próximo é exibido na posição atual quando não está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="3b464-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="3b464-122">O estado padrão é false.</span><span class="sxs-lookup"><span data-stu-id="3b464-122">Default state is false.</span></span> <span data-ttu-id="3b464-123">Não tem nenhum efeito nas faixas de áudio.</span><span class="sxs-lookup"><span data-stu-id="3b464-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="3b464-124">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="3b464-124">shuffle</span></span>    | <span data-ttu-id="3b464-125">Modo que indica se as faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="3b464-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="3b464-126">O estado padrão é false.</span><span class="sxs-lookup"><span data-stu-id="3b464-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="3b464-127">*estado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b464-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b464-128">**Booliano** que especifica se o novo modo especificado está ativo ou não.</span><span class="sxs-lookup"><span data-stu-id="3b464-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b464-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b464-129">Return value</span></span>

<span data-ttu-id="3b464-130">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3b464-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b464-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b464-131">Remarks</span></span>

<span data-ttu-id="3b464-132">Quando o modo de conquadro é ativo, o Player deve acessar o conteúdo da faixa para recuperar o quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b464-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="3b464-133">Devido a considerações de largura de banda, use esse modo com cuidado ao reproduzir conteúdo não local.</span><span class="sxs-lookup"><span data-stu-id="3b464-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b464-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b464-134">Requirements</span></span>



| <span data-ttu-id="3b464-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b464-135">Requirement</span></span> | <span data-ttu-id="3b464-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3b464-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b464-137">Versão</span><span class="sxs-lookup"><span data-stu-id="3b464-137">Version</span></span><br/> | <span data-ttu-id="3b464-138">Para modos de loop e ordem aleatória, Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3b464-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="3b464-139">Para modos de autoretrocesso e de conframe, o Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3b464-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="3b464-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3b464-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b464-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b464-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="3b464-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b464-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b464-143">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="3b464-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="3b464-144">**Settings. GetMode**</span><span class="sxs-lookup"><span data-stu-id="3b464-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





