---
description: As constantes de sinalizador de bit PHONEBUTTONSTATE descrevem as posições dos botões.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Constantes de PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788046"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="45140-103">PHONEBUTTONSTATE_ constantes</span><span class="sxs-lookup"><span data-stu-id="45140-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="45140-104">As constantes de sinalizador de bit **PHONEBUTTONSTATE_** descrevem as posições do botão.</span><span class="sxs-lookup"><span data-stu-id="45140-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="45140-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="45140-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45140-106">O botão está no estado "Down" (pressionado).</span><span class="sxs-lookup"><span data-stu-id="45140-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45140-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="45140-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45140-108">Indica que o estado para cima ou para baixo do botão não é conhecido pelo provedor de serviços e não se tornará conhecido em um momento futuro.</span><span class="sxs-lookup"><span data-stu-id="45140-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="45140-109">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="45140-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45140-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="45140-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45140-111">Indica que o estado ativo ou inativo do botão não é conhecido neste momento, mas pode ser conhecido em um momento futuro.</span><span class="sxs-lookup"><span data-stu-id="45140-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="45140-112">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="45140-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="45140-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="45140-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="45140-114">O botão está no estado "para cima".</span><span class="sxs-lookup"><span data-stu-id="45140-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45140-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="45140-115">Remarks</span></span>

<span data-ttu-id="45140-116">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="45140-116">No extensibility.</span></span> <span data-ttu-id="45140-117">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="45140-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="45140-118">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada no telefone e não usar esses PHONEBUTTONSTATE_ valores para os quais a versão negociada não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="45140-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="45140-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45140-119">Requirements</span></span>



| <span data-ttu-id="45140-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45140-120">Requirement</span></span> | <span data-ttu-id="45140-121">Valor</span><span class="sxs-lookup"><span data-stu-id="45140-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="45140-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="45140-122">TAPI version</span></span><br/> | <span data-ttu-id="45140-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="45140-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="45140-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45140-124">Header</span></span><br/>       | <dl> <span data-ttu-id="45140-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="45140-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




