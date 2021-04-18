---
title: Evento Player. AudioLanguageChange
description: O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Evento AudioLanguageChange do Windows Media Player
- Evento AudioLanguageChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763059"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="3adbb-107">Evento Player. AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="3adbb-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="3adbb-108">O evento **AudioLanguageChange** ocorre quando o idioma de áudio atual é alterado.</span><span class="sxs-lookup"><span data-stu-id="3adbb-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adbb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3adbb-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="3adbb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3adbb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adbb-111">*LangID*</span><span class="sxs-lookup"><span data-stu-id="3adbb-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="3adbb-112">**Número** (**longo**) que especifica o novo LCID (identificador de localidade).</span><span class="sxs-lookup"><span data-stu-id="3adbb-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adbb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3adbb-113">Return value</span></span>

<span data-ttu-id="3adbb-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3adbb-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3adbb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3adbb-115">Remarks</span></span>

<span data-ttu-id="3adbb-116">Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.</span><span class="sxs-lookup"><span data-stu-id="3adbb-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="3adbb-117">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou passado para um método em um arquivo Microsoft JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="3adbb-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="3adbb-118">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="3adbb-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="3adbb-119">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="3adbb-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="3adbb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3adbb-120">Requirements</span></span>



| <span data-ttu-id="3adbb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3adbb-121">Requirement</span></span> | <span data-ttu-id="3adbb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3adbb-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3adbb-123">Versão</span><span class="sxs-lookup"><span data-stu-id="3adbb-123">Version</span></span><br/> | <span data-ttu-id="3adbb-124">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3adbb-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="3adbb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3adbb-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3adbb-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3adbb-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adbb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3adbb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adbb-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="3adbb-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="3adbb-129">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="3adbb-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





