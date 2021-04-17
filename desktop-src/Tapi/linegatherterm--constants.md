---
description: As \_ constantes de sinalizador de bit LINEGATHERTERM descrevem as condições sob as quais a coleta de dígitos em buffer é encerrada.
ms.assetid: 409e1984-e5a4-4636-ab53-5973fe7b78ea
title: Constantes de LINEGATHERTERM_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968492a584024c7750b417a9fd03b68ac1df42ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783359"
---
# <a name="linegatherterm_-constants"></a><span data-ttu-id="f05db-103">\_Constantes LINEGATHERTERM</span><span class="sxs-lookup"><span data-stu-id="f05db-103">LINEGATHERTERM\_ Constants</span></span>

<span data-ttu-id="f05db-104">As constantes de sinalizador de bit **LINEGATHERTERM \_** descrevem as condições sob as quais a coleta de dígitos em buffer é encerrada.</span><span class="sxs-lookup"><span data-stu-id="f05db-104">The **LINEGATHERTERM\_** bit-flag constants describe the conditions under which buffered digit gathering is terminated.</span></span>

<dl> <dt>

<span data-ttu-id="f05db-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM \_ BUFFERFULL**</span><span class="sxs-lookup"><span data-stu-id="f05db-105"><span id="LINEGATHERTERM_BUFFERFULL"></span><span id="linegatherterm_bufferfull"></span>**LINEGATHERTERM\_BUFFERFULL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f05db-106">O número de dígitos solicitado foi coletado.</span><span class="sxs-lookup"><span data-stu-id="f05db-106">The requested number of digits has been gathered.</span></span> <span data-ttu-id="f05db-107">O buffer está cheio.</span><span class="sxs-lookup"><span data-stu-id="f05db-107">The buffer is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f05db-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM \_ cancelar**</span><span class="sxs-lookup"><span data-stu-id="f05db-108"><span id="LINEGATHERTERM_CANCEL"></span><span id="linegatherterm_cancel"></span>**LINEGATHERTERM\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f05db-109">A solicitação foi cancelada por este aplicativo, por outro aplicativo ou porque a chamada foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="f05db-109">The request was canceled by this application, by another application, or because the call terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f05db-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM \_ FIRSTTIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="f05db-110"><span id="LINEGATHERTERM_FIRSTTIMEOUT"></span><span id="linegatherterm_firsttimeout"></span>**LINEGATHERTERM\_FIRSTTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f05db-111">O tempo limite do primeiro dígito expirou.</span><span class="sxs-lookup"><span data-stu-id="f05db-111">The first digit timeout expired.</span></span> <span data-ttu-id="f05db-112">O buffer não contém dígitos.</span><span class="sxs-lookup"><span data-stu-id="f05db-112">The buffer contains no digits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f05db-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**intertempo de LINEGATHERTERM \_**</span><span class="sxs-lookup"><span data-stu-id="f05db-113"><span id="LINEGATHERTERM_INTERTIMEOUT"></span><span id="linegatherterm_intertimeout"></span>**LINEGATHERTERM\_INTERTIMEOUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f05db-114">O tempo limite entre dígitos expirou.</span><span class="sxs-lookup"><span data-stu-id="f05db-114">The inter-digit timeout expired.</span></span> <span data-ttu-id="f05db-115">O buffer contém pelo menos um dígito.</span><span class="sxs-lookup"><span data-stu-id="f05db-115">The buffer contains at least one digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f05db-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM \_ TERMDIGIT**</span><span class="sxs-lookup"><span data-stu-id="f05db-116"><span id="LINEGATHERTERM_TERMDIGIT"></span><span id="linegatherterm_termdigit"></span>**LINEGATHERTERM\_TERMDIGIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f05db-117">Um dos dígitos de encerramento correspondeu a um dígito recebido.</span><span class="sxs-lookup"><span data-stu-id="f05db-117">One of the termination digits matched a received digit.</span></span> <span data-ttu-id="f05db-118">O dígito de terminação correspondente é o último dígito no buffer.</span><span class="sxs-lookup"><span data-stu-id="f05db-118">The matched termination digit is the last digit in the buffer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f05db-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f05db-119">Remarks</span></span>

<span data-ttu-id="f05db-120">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="f05db-120">No extensibility.</span></span> <span data-ttu-id="f05db-121">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="f05db-121">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05db-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f05db-122">Requirements</span></span>



| <span data-ttu-id="f05db-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05db-123">Requirement</span></span> | <span data-ttu-id="f05db-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f05db-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f05db-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="f05db-125">TAPI version</span></span><br/> | <span data-ttu-id="f05db-126">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f05db-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f05db-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f05db-127">Header</span></span><br/>       | <dl> <span data-ttu-id="f05db-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f05db-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




