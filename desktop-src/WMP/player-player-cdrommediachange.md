---
title: Evento Player. CdromMediaChange
description: O evento CdromMediaChange ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Evento CdromMediaChange do Windows Media Player
- Evento CdromMediaChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813660"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="dda2c-107">Evento Player. CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="dda2c-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="dda2c-108">O evento **CdromMediaChange** ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="dda2c-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="dda2c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dda2c-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="dda2c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dda2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda2c-111">*CdromNum*</span><span class="sxs-lookup"><span data-stu-id="dda2c-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="dda2c-112">**Número** (**longo**) especificando o índice da unidade de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="dda2c-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda2c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dda2c-113">Return value</span></span>

<span data-ttu-id="dda2c-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dda2c-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda2c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dda2c-115">Remarks</span></span>

<span data-ttu-id="dda2c-116">O índice da unidade de CD corresponde ao índice de um objeto de **cdrom** na **cdromCollection**.</span><span class="sxs-lookup"><span data-stu-id="dda2c-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="dda2c-117">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="dda2c-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="dda2c-118">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="dda2c-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="dda2c-119">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="dda2c-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda2c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dda2c-120">Requirements</span></span>



| <span data-ttu-id="dda2c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda2c-121">Requirement</span></span> | <span data-ttu-id="dda2c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dda2c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dda2c-123">Versão</span><span class="sxs-lookup"><span data-stu-id="dda2c-123">Version</span></span><br/> | <span data-ttu-id="dda2c-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dda2c-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dda2c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dda2c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="dda2c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dda2c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda2c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dda2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda2c-128">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="dda2c-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="dda2c-129">**Objeto cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="dda2c-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="dda2c-130">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="dda2c-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





