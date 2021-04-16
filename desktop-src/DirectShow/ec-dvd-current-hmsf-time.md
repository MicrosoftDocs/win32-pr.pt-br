---
description: Sinaliza a hora atual, no formato de código de tempo HMSF do DVD \_ \_ , em relação ao início do título. Esse evento é disparado no início de cada VOBU, que ocorre a cada 0,4 a 1,0 segundos.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758068"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="4172a-104">\_hora de \_ \_ HMSF atual do DVD \_ do EC</span><span class="sxs-lookup"><span data-stu-id="4172a-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="4172a-105">Sinaliza a hora atual, no formato de [**\_ \_ código**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) de tempo HMSF do DVD, em relação ao início do título.</span><span class="sxs-lookup"><span data-stu-id="4172a-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="4172a-106">Esse evento é disparado no início de cada VOBU, que ocorre a cada 0,4 a 1,0 segundos.</span><span class="sxs-lookup"><span data-stu-id="4172a-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="4172a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4172a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4172a-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4172a-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4172a-109">Um valor ULONG que contém a estrutura do código de HMSF do DVD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4172a-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="4172a-110">Atribua lParam1 a uma variável ULONG e, em seguida, converta essa variável em um código de HMSF de DVD \_ \_ para acessar seus valores.</span><span class="sxs-lookup"><span data-stu-id="4172a-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="4172a-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4172a-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4172a-112">Um valor ULONG que contém uma União [**de \_ \_ sinalizadores de código**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)de paficação de DVD.</span><span class="sxs-lookup"><span data-stu-id="4172a-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4172a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4172a-113">Remarks</span></span>

<span data-ttu-id="4172a-114">O \_ formato do código de tempo HMSF do DVD \_ é destinado a substituir o antigo formato BCD que é retornado nos \_ eventos de hora atual do DVD do EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4172a-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="4172a-115">É mais fácil trabalhar com os códigos de timeHMSF.</span><span class="sxs-lookup"><span data-stu-id="4172a-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="4172a-116">Para fazer com que o navegador \_ envie \_ \_ eventos de \_ hora de HMSF atuais em vez dos \_ eventos de hora atual do DVD do EC \_ \_ , um aplicativo deve chamar `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` .</span><span class="sxs-lookup"><span data-stu-id="4172a-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="4172a-117">Quando esse sinalizador é definido, o navegador também esperará que todos os parâmetros de tempo nos métodos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) sejam passados como \_ \_ timecódigos de DVD HMSF.</span><span class="sxs-lookup"><span data-stu-id="4172a-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="4172a-118">Esse evento é gerado nos domínios de título.</span><span class="sxs-lookup"><span data-stu-id="4172a-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="4172a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4172a-119">Requirements</span></span>



| <span data-ttu-id="4172a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4172a-120">Requirement</span></span> | <span data-ttu-id="4172a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4172a-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4172a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4172a-122">Header</span></span><br/> | <dl> <span data-ttu-id="4172a-123"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4172a-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4172a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4172a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4172a-125">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="4172a-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="4172a-126">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="4172a-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4172a-127">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4172a-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




