---
description: As \_ constantes de sinalizador de bit LINETERMMODE descrevem diferentes tipos de eventos em uma linha telefônica que pode ser roteada para um dispositivo de terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes de LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766971"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="b4326-103">\_Constantes LINETERMMODE</span><span class="sxs-lookup"><span data-stu-id="b4326-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="b4326-104">As constantes de sinalizador de bit **LINETERMMODE \_** descrevem diferentes tipos de eventos em uma linha telefônica que pode ser roteada para um dispositivo de terminal.</span><span class="sxs-lookup"><span data-stu-id="b4326-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="b4326-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**botões de LINETERMMODE \_**</span><span class="sxs-lookup"><span data-stu-id="b4326-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-106">Esses são eventos de pressionamento de botão enviados do terminal para a linha.</span><span class="sxs-lookup"><span data-stu-id="b4326-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**exibição do LINETERMMODE \_**</span><span class="sxs-lookup"><span data-stu-id="b4326-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-108">Essas são informações de exibição enviadas da linha para o terminal.</span><span class="sxs-lookup"><span data-stu-id="b4326-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**</span><span class="sxs-lookup"><span data-stu-id="b4326-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-110">Esses são eventos Hookswitch enviados do terminal para a linha.</span><span class="sxs-lookup"><span data-stu-id="b4326-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**lâmpadas LINETERMMODEs \_**</span><span class="sxs-lookup"><span data-stu-id="b4326-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-112">Esses são eventos de lâmpada enviados da linha para o terminal.</span><span class="sxs-lookup"><span data-stu-id="b4326-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="b4326-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-114">Esse é o fluxo de mídia bidirecional associado a uma chamada na linha e no terminal.</span><span class="sxs-lookup"><span data-stu-id="b4326-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="b4326-115">Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada não puder ser controlado independentemente.</span><span class="sxs-lookup"><span data-stu-id="b4326-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**</span><span class="sxs-lookup"><span data-stu-id="b4326-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-117">Esse é o fluxo de mídia unidirecional da linha para o terminal associado a uma chamada na linha.</span><span class="sxs-lookup"><span data-stu-id="b4326-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="b4326-118">Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada puder ser controlado independentemente.</span><span class="sxs-lookup"><span data-stu-id="b4326-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**</span><span class="sxs-lookup"><span data-stu-id="b4326-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-120">Esse é o fluxo de mídia unidirecional do terminal para a linha associada a uma chamada na linha.</span><span class="sxs-lookup"><span data-stu-id="b4326-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="b4326-121">Use esse valor quando o roteamento de ambos os canais unidirecionais do fluxo de mídia de uma chamada puder ser controlado independentemente.</span><span class="sxs-lookup"><span data-stu-id="b4326-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b4326-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_toque LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="b4326-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b4326-123">Essas são as informações de controle de toque enviadas do comutador para o terminal.</span><span class="sxs-lookup"><span data-stu-id="b4326-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4326-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4326-124">Remarks</span></span>

<span data-ttu-id="b4326-125">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="b4326-125">No extensibility.</span></span> <span data-ttu-id="b4326-126">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="b4326-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="b4326-127">Essas constantes descrevem as classes de fluxo de controle e de informações que podem ser roteadas diretamente entre um dispositivo de linha e um dispositivo de terminal (como um conjunto de telefone).</span><span class="sxs-lookup"><span data-stu-id="b4326-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4326-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4326-128">Requirements</span></span>



| <span data-ttu-id="b4326-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4326-129">Requirement</span></span> | <span data-ttu-id="b4326-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b4326-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b4326-131">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b4326-131">TAPI version</span></span><br/> | <span data-ttu-id="b4326-132">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b4326-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b4326-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4326-133">Header</span></span><br/>       | <dl> <span data-ttu-id="b4326-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4326-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 




