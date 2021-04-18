---
description: As \_ constantes de sinalizador de bit LINECALLCOMPLMODE descrevem diferentes maneiras em que uma chamada pode ser concluída.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Constantes de LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767745"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="df900-103">\_Constantes LINECALLCOMPLMODE</span><span class="sxs-lookup"><span data-stu-id="df900-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="df900-104">As constantes de sinalizador de bit **LINECALLCOMPLMODE \_** descrevem diferentes maneiras em que uma chamada pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="df900-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="df900-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_retorno de chamada LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="df900-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="df900-106">Solicita que a estação chamada retorne a chamada quando ela retornar para ocioso.</span><span class="sxs-lookup"><span data-stu-id="df900-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="df900-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ Camp**</span><span class="sxs-lookup"><span data-stu-id="df900-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="df900-108">Enfileira a chamada até que a chamada possa ser concluída.</span><span class="sxs-lookup"><span data-stu-id="df900-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="df900-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**intrusão LINECALLCOMPLMODE \_**</span><span class="sxs-lookup"><span data-stu-id="df900-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="df900-110">Adiciona o aplicativo à chamada existente na estação chamada (Barge).</span><span class="sxs-lookup"><span data-stu-id="df900-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="df900-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_mensagem LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="df900-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="df900-112">Deixa uma mensagem predefinida curta para a estação chamada (Deixe o Word chamar).</span><span class="sxs-lookup"><span data-stu-id="df900-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="df900-113">A mensagem a ser enviada é especificada separadamente.</span><span class="sxs-lookup"><span data-stu-id="df900-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df900-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="df900-114">Remarks</span></span>

<span data-ttu-id="df900-115">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="df900-115">No extensibility.</span></span> <span data-ttu-id="df900-116">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="df900-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="df900-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df900-117">Requirements</span></span>



| <span data-ttu-id="df900-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df900-118">Requirement</span></span> | <span data-ttu-id="df900-119">Valor</span><span class="sxs-lookup"><span data-stu-id="df900-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="df900-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="df900-120">TAPI version</span></span><br/> | <span data-ttu-id="df900-121">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="df900-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="df900-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df900-122">Header</span></span><br/>       | <dl> <span data-ttu-id="df900-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="df900-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




