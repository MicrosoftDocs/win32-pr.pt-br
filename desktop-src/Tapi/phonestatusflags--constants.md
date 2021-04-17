---
description: As \_ constantes de sinalizador de bit PHONESTATUSFLAGS descrevem uma variedade de informações de status do dispositivo de telefone.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes de PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811922"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="94581-103">\_Constantes PHONESTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="94581-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="94581-104">As constantes de sinalizador de bit **PHONESTATUSFLAGS \_** descrevem uma variedade de informações de status do dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="94581-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="94581-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="94581-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94581-106">Especifica se o telefone está atualmente conectado à TAPI.</span><span class="sxs-lookup"><span data-stu-id="94581-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="94581-107">**True** se conectado; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="94581-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="94581-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspensa**</span><span class="sxs-lookup"><span data-stu-id="94581-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="94581-109">Especifica se a manipulação da TAPI do dispositivo de telefone está suspensa.</span><span class="sxs-lookup"><span data-stu-id="94581-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="94581-110">**True** se suspenso; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="94581-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="94581-111">O uso do aplicativo de um dispositivo telefônico pode ser temporariamente suspenso quando o comutador deseja manipular o telefone de forma que não possa tolerar a interferência do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94581-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94581-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="94581-112">Remarks</span></span>

<span data-ttu-id="94581-113">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="94581-113">No extensibility.</span></span> <span data-ttu-id="94581-114">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="94581-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="94581-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94581-115">Requirements</span></span>



| <span data-ttu-id="94581-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="94581-116">Requirement</span></span> | <span data-ttu-id="94581-117">Valor</span><span class="sxs-lookup"><span data-stu-id="94581-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="94581-118">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="94581-118">TAPI version</span></span><br/> | <span data-ttu-id="94581-119">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="94581-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="94581-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94581-120">Header</span></span><br/>       | <dl> <span data-ttu-id="94581-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="94581-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




