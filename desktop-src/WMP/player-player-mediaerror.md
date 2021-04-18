---
title: Evento Player. MediaError
description: O evento MediaError ocorre quando o objeto de mídia tem uma condição de erro.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Evento MediaError do Windows Media Player
- Evento MediaError Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810827"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="25de7-106">Evento Player. MediaError</span><span class="sxs-lookup"><span data-stu-id="25de7-106">Player.MediaError event</span></span>

<span data-ttu-id="25de7-107">O evento **MediaError** ocorre quando o objeto de **mídia** tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="25de7-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="25de7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25de7-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="25de7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25de7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25de7-110">*pMediaObject*</span><span class="sxs-lookup"><span data-stu-id="25de7-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="25de7-111">Objeto de **mídia** que tem uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="25de7-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25de7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25de7-112">Return value</span></span>

<span data-ttu-id="25de7-113">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="25de7-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25de7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25de7-114">Remarks</span></span>

<span data-ttu-id="25de7-115">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="25de7-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="25de7-116">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="25de7-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="25de7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25de7-117">Requirements</span></span>



| <span data-ttu-id="25de7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="25de7-118">Requirement</span></span> | <span data-ttu-id="25de7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="25de7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="25de7-120">Versão</span><span class="sxs-lookup"><span data-stu-id="25de7-120">Version</span></span><br/> | <span data-ttu-id="25de7-121">Windows Media Player para Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="25de7-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="25de7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="25de7-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="25de7-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25de7-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25de7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="25de7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25de7-125">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="25de7-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





