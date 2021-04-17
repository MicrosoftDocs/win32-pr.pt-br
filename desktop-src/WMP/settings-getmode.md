---
title: Método Settings. GetMode
description: O método GetMode determina se o modo de loop ou de ordem aleatória está ativo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- método GetMode do Windows Media Player
- método GetMode Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método GetMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748093"
---
# <a name="settingsgetmode-method"></a><span data-ttu-id="8f393-106">Método Settings. GetMode</span><span class="sxs-lookup"><span data-stu-id="8f393-106">Settings.getMode method</span></span>

<span data-ttu-id="8f393-107">O método **GetMode** determina se o modo de loop ou de ordem aleatória está ativo.</span><span class="sxs-lookup"><span data-stu-id="8f393-107">The **getMode** method determines whether the loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f393-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f393-108">Syntax</span></span>


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a><span data-ttu-id="8f393-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f393-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f393-110">*modeName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f393-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f393-111">**Cadeia de caracteres** que especifica o nome do modo em questão, contendo um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f393-111">**String** specifying the name of the mode in question, containing one of the following values.</span></span>



| <span data-ttu-id="8f393-112">String</span><span class="sxs-lookup"><span data-stu-id="8f393-112">String</span></span>     | <span data-ttu-id="8f393-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f393-113">Description</span></span>                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f393-114">rebobinar</span><span class="sxs-lookup"><span data-stu-id="8f393-114">autoRewind</span></span> | <span data-ttu-id="8f393-115">As faixas são reiniciadas no início depois da reprodução até o fim.</span><span class="sxs-lookup"><span data-stu-id="8f393-115">Tracks are restarted at the beginning after playing to the end.</span></span>                                                          |
| <span data-ttu-id="8f393-116">loop</span><span class="sxs-lookup"><span data-stu-id="8f393-116">loop</span></span>       | <span data-ttu-id="8f393-117">A sequência de faixas se repete.</span><span class="sxs-lookup"><span data-stu-id="8f393-117">The sequence of tracks repeats itself.</span></span>                                                                                   |
| <span data-ttu-id="8f393-118">conmoldura</span><span class="sxs-lookup"><span data-stu-id="8f393-118">showFrame</span></span>  | <span data-ttu-id="8f393-119">O quadro de chave mais próximo é exibido na posição atual quando não está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8f393-119">The nearest key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="8f393-120">Esse modo não é relevante para faixas de áudio.</span><span class="sxs-lookup"><span data-stu-id="8f393-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="8f393-121">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="8f393-121">shuffle</span></span>    | <span data-ttu-id="8f393-122">As faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="8f393-122">Tracks are played in random order.</span></span>                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f393-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f393-123">Return value</span></span>

<span data-ttu-id="8f393-124">Esse método retorna um valor **booliano** que indica se o modo especificado está ativo.</span><span class="sxs-lookup"><span data-stu-id="8f393-124">This method returns a **Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f393-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f393-125">Requirements</span></span>



| <span data-ttu-id="8f393-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f393-126">Requirement</span></span> | <span data-ttu-id="8f393-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8f393-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f393-128">Versão</span><span class="sxs-lookup"><span data-stu-id="8f393-128">Version</span></span><br/> | <span data-ttu-id="8f393-129">Para modos de loop e ordem aleatória, Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8f393-129">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="8f393-130">Para modos de autoretrocesso e de conframe, o Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8f393-130">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="8f393-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8f393-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8f393-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f393-132"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="8f393-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f393-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f393-134">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="8f393-134">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="8f393-135">**Settings. setmode**</span><span class="sxs-lookup"><span data-stu-id="8f393-135">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





