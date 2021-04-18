---
description: Ocorreu um erro de dispositivo em um filtro de processador de áudio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1182aaba7bb30ad27511b47ba8e4432d8fd33da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751876"
---
# <a name="ec_snddev_out_error"></a><span data-ttu-id="097d0-103">erro do EC \_ SNDDEV \_ out \_</span><span class="sxs-lookup"><span data-stu-id="097d0-103">EC\_SNDDEV\_OUT\_ERROR</span></span>

<span data-ttu-id="097d0-104">Ocorreu um erro de dispositivo em um filtro de processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="097d0-104">A device error has occurred in an audio renderer filter.</span></span>

## <a name="parameters"></a><span data-ttu-id="097d0-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="097d0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097d0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="097d0-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="097d0-107">Valor DWORD do tipo enumerado [**SNDDEV \_ Err**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) , indicando como o dispositivo estava sendo acessado quando a falha ocorreu.</span><span class="sxs-lookup"><span data-stu-id="097d0-107">DWORD value from the [**SNDDEV\_ERR**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) enumerated type, indicating how the device was being accessed when the failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="097d0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="097d0-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="097d0-109">Valor DWORD que indica o erro retornado da chamada do dispositivo de som.</span><span class="sxs-lookup"><span data-stu-id="097d0-109">DWORD value indicating the error returned from the sound device call.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="097d0-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="097d0-110">Default Action</span></span>

<span data-ttu-id="097d0-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="097d0-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="097d0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="097d0-112">Requirements</span></span>



| <span data-ttu-id="097d0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="097d0-113">Requirement</span></span> | <span data-ttu-id="097d0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="097d0-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="097d0-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="097d0-115">Header</span></span><br/> | <dl> <span data-ttu-id="097d0-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="097d0-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097d0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="097d0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097d0-118">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="097d0-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="097d0-119">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="097d0-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




