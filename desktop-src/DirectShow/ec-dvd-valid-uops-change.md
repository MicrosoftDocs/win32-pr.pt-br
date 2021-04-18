---
description: Sinaliza que o conjunto disponível de métodos de interface IDvdControl2 foi alterado.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752068"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="92bc2-103">\_ \_ \_ alteração UOPS válida do DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="92bc2-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="92bc2-104">Sinaliza que o conjunto disponível de métodos de interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) foi alterado.</span><span class="sxs-lookup"><span data-stu-id="92bc2-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="92bc2-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92bc2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92bc2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="92bc2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="92bc2-107">Valor **DWORD** que contém uma combinação de zero ou mais sinalizadores da enumeração [**de \_ \_ sinalizador UOP válida**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) .</span><span class="sxs-lookup"><span data-stu-id="92bc2-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="92bc2-108">Os bits indicam quais comandos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) foram explicitamente desabilitados pelo disco DVD.</span><span class="sxs-lookup"><span data-stu-id="92bc2-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="92bc2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="92bc2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="92bc2-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="92bc2-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92bc2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="92bc2-111">Remarks</span></span>

<span data-ttu-id="92bc2-112">Esse evento indica apenas quais operações são explicitamente desabilitadas pelo conteúdo no disco DVD. Ele não garante que seja válido chamar métodos que não estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="92bc2-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="92bc2-113">Por exemplo, se nenhum botão estiver presente, o método [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) não funcionará, embora o método não esteja explicitamente desabilitado.</span><span class="sxs-lookup"><span data-stu-id="92bc2-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="92bc2-114">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="92bc2-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="92bc2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92bc2-115">Requirements</span></span>



| <span data-ttu-id="92bc2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92bc2-116">Requirement</span></span> | <span data-ttu-id="92bc2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="92bc2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92bc2-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92bc2-118">Header</span></span><br/> | <dl> <span data-ttu-id="92bc2-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92bc2-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92bc2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="92bc2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92bc2-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="92bc2-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="92bc2-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="92bc2-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="92bc2-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="92bc2-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




