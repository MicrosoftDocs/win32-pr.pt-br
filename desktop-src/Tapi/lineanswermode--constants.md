---
description: As \_ constantes de sinalizador de bit LINEANSWERMODE descrevem como uma chamada ativa existente em um dispositivo de linha é afetada respondendo a outra chamada de oferta na mesma linha.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes de LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757220"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="9440c-103">\_Constantes LINEANSWERMODE</span><span class="sxs-lookup"><span data-stu-id="9440c-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="9440c-104">As constantes de sinalizador de bit **LINEANSWERMODE \_** descrevem como uma chamada ativa existente em um dispositivo de linha é afetada respondendo a outra chamada de *oferta* na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="9440c-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="9440c-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**\_descartar LINEANSWERMODE**</span><span class="sxs-lookup"><span data-stu-id="9440c-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9440c-106">A chamada ativa no momento será automaticamente descartada.</span><span class="sxs-lookup"><span data-stu-id="9440c-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9440c-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_ reter**</span><span class="sxs-lookup"><span data-stu-id="9440c-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9440c-108">A chamada ativa no momento será automaticamente colocada em espera.</span><span class="sxs-lookup"><span data-stu-id="9440c-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9440c-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="9440c-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="9440c-110">Responder a outra chamada na mesma linha não tem nenhum efeito sobre a chamada ativa existente na linha.</span><span class="sxs-lookup"><span data-stu-id="9440c-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9440c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9440c-111">Remarks</span></span>

<span data-ttu-id="9440c-112">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="9440c-112">No extensibility.</span></span> <span data-ttu-id="9440c-113">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="9440c-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="9440c-114">Se uma chamada chegar (é oferecida) no momento em que outra chamada já estiver ativa, a nova chamada será conectada invocando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="9440c-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="9440c-115">O efeito que isso tem na chamada ativa existente depende dos recursos do dispositivo da linha.</span><span class="sxs-lookup"><span data-stu-id="9440c-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="9440c-116">A primeira chamada pode não ser afetada, pode ser descartada automaticamente ou pode ser automaticamente colocada em espera.</span><span class="sxs-lookup"><span data-stu-id="9440c-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="9440c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9440c-117">Requirements</span></span>



| <span data-ttu-id="9440c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9440c-118">Requirement</span></span> | <span data-ttu-id="9440c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9440c-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9440c-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="9440c-120">TAPI version</span></span><br/> | <span data-ttu-id="9440c-121">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9440c-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="9440c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9440c-122">Header</span></span><br/>       | <dl> <span data-ttu-id="9440c-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9440c-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




