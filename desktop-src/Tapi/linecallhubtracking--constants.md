---
description: As \_ constantes de sinalizador de bit LINECALLHUBTRACKING descrevem o tipo de rastreamento de Hub de chamada fornecido.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes de LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758402"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="4a257-103">\_Constantes LINECALLHUBTRACKING</span><span class="sxs-lookup"><span data-stu-id="4a257-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="4a257-104">As constantes de sinalizador de bit **LINECALLHUBTRACKING \_** descrevem o tipo de rastreamento de Hub de chamada fornecido.</span><span class="sxs-lookup"><span data-stu-id="4a257-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="4a257-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING de \_ chamadas**</span><span class="sxs-lookup"><span data-stu-id="4a257-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4a257-106">O controle do hub de chamadas é fornecido no nível de chamada.</span><span class="sxs-lookup"><span data-stu-id="4a257-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a257-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="4a257-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4a257-108">Nenhum controle de Hub de chamadas é fornecido.</span><span class="sxs-lookup"><span data-stu-id="4a257-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a257-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**</span><span class="sxs-lookup"><span data-stu-id="4a257-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4a257-110">Os hubs de chamadas são controlados no nível do provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="4a257-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="4a257-111">As alterações de chamada por chamada não são relatadas.</span><span class="sxs-lookup"><span data-stu-id="4a257-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a257-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a257-112">Remarks</span></span>

<span data-ttu-id="4a257-113">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="4a257-113">No extensibility.</span></span> <span data-ttu-id="4a257-114">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="4a257-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="4a257-115">Quando ocorrem alterações nessa estrutura de dados, uma mensagem de [**\_ CALLINFO de linha**](line-callinfo.md) é enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a257-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="4a257-116">Os parâmetros para essa mensagem são um identificador para a chamada e uma indicação do item de informações que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4a257-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="4a257-117">A estrutura de dados [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica qual tipo de rastreamento é fornecido.</span><span class="sxs-lookup"><span data-stu-id="4a257-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a257-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a257-118">Requirements</span></span>



| <span data-ttu-id="4a257-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a257-119">Requirement</span></span> | <span data-ttu-id="4a257-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4a257-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4a257-121">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="4a257-121">TAPI version</span></span><br/> | <span data-ttu-id="4a257-122">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="4a257-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4a257-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a257-123">Header</span></span><br/>       | <dl> <span data-ttu-id="4a257-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a257-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a257-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a257-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a257-126">**CALLINFO de linha \_**</span><span class="sxs-lookup"><span data-stu-id="4a257-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="4a257-127">**LINECALLHUBTRACKINGINFO**</span><span class="sxs-lookup"><span data-stu-id="4a257-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="4a257-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="4a257-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




