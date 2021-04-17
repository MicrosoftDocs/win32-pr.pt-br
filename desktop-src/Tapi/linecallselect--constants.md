---
description: As \_ constantes de sinalizador de bit LINECALLSELECT descrevem quais chamadas devem ser selecionadas.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes de LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768571"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="8b1e8-103">\_Constantes LINECALLSELECT</span><span class="sxs-lookup"><span data-stu-id="8b1e8-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="8b1e8-104">As constantes de sinalizador de bit **LINECALLSELECT \_** descrevem quais chamadas devem ser selecionadas.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="8b1e8-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_endereço LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="8b1e8-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b1e8-106">Seleciona a chamada no endereço especificado.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b1e8-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_chamada LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="8b1e8-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b1e8-108">Seleciona chamadas relacionadas à chamada especificada.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="8b1e8-109">Por exemplo, as partes em uma chamada de conferência.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b1e8-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**\_callid LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="8b1e8-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b1e8-111">Seleciona chamadas relacionadas ao identificador de chamada especificado.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="8b1e8-112">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b1e8-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8b1e8-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b1e8-114">Seleciona chamadas no identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="8b1e8-115">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="8b1e8-116">Os aplicativos devem considerar o uso da \_ constante de linha LINECALLSELECT em vez deste.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8b1e8-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ linha**</span><span class="sxs-lookup"><span data-stu-id="8b1e8-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8b1e8-118">Seleciona as chamadas no dispositivo de linha especificado.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b1e8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b1e8-119">Remarks</span></span>

<span data-ttu-id="8b1e8-120">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-120">No extensibility.</span></span> <span data-ttu-id="8b1e8-121">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="8b1e8-122">Essa constante é usada em [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) e para especificar uma seleção (escopo) das chamadas que são solicitadas.</span><span class="sxs-lookup"><span data-stu-id="8b1e8-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1e8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b1e8-123">Requirements</span></span>



| <span data-ttu-id="8b1e8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b1e8-124">Requirement</span></span> | <span data-ttu-id="8b1e8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8b1e8-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8b1e8-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8b1e8-126">TAPI version</span></span><br/> | <span data-ttu-id="8b1e8-127">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8b1e8-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8b1e8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b1e8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="8b1e8-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b1e8-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




