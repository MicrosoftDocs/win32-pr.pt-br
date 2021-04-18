---
title: Evento Player. MarkerHit
description: O evento MarkerHit ocorre quando um marcador é atingido. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Evento MarkerHit do Windows Media Player
- Evento MarkerHit Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760431"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="d2385-107">Evento Player. MarkerHit</span><span class="sxs-lookup"><span data-stu-id="d2385-107">Player.MarkerHit event</span></span>

<span data-ttu-id="d2385-108">O evento **MarkerHit** ocorre quando um marcador é atingido.</span><span class="sxs-lookup"><span data-stu-id="d2385-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2385-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2385-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="d2385-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2385-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2385-111">*MarkerNum*</span><span class="sxs-lookup"><span data-stu-id="d2385-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="d2385-112">**Número** (**longo**) indicando o número do marcador que foi atingido.</span><span class="sxs-lookup"><span data-stu-id="d2385-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2385-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2385-113">Return value</span></span>

<span data-ttu-id="d2385-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2385-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2385-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2385-115">Remarks</span></span>

<span data-ttu-id="d2385-116">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="d2385-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d2385-117">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="d2385-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2385-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2385-118">Requirements</span></span>



| <span data-ttu-id="d2385-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2385-119">Requirement</span></span> | <span data-ttu-id="d2385-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d2385-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d2385-121">Versão</span><span class="sxs-lookup"><span data-stu-id="d2385-121">Version</span></span><br/> | <span data-ttu-id="d2385-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d2385-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d2385-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d2385-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2385-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2385-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2385-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2385-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2385-126">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="d2385-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





