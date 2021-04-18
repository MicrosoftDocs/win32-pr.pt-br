---
description: Sinaliza que o número do fluxo de áudio atual foi alterado para o título principal do DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757302"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="40758-103">\_alteração de \_ fluxo de áudio \_ \_ do EC DVD</span><span class="sxs-lookup"><span data-stu-id="40758-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="40758-104">Sinaliza que o número do fluxo de áudio atual foi alterado para o título principal do DVD.</span><span class="sxs-lookup"><span data-stu-id="40758-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="40758-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40758-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40758-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="40758-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="40758-107">Valor **DWORD** que indica o novo número de fluxo de áudio do usuário.</span><span class="sxs-lookup"><span data-stu-id="40758-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="40758-108">Os números de fluxo de áudio variam de 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="40758-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="40758-109">O fluxo 0xFFFFFFFF indica que nenhum fluxo está selecionado.</span><span class="sxs-lookup"><span data-stu-id="40758-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="40758-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="40758-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="40758-111">Zero.</span><span class="sxs-lookup"><span data-stu-id="40758-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40758-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="40758-112">Remarks</span></span>

<span data-ttu-id="40758-113">O fluxo de áudio atual pode ser alterado automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="40758-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="40758-114">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="40758-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="40758-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40758-115">Requirements</span></span>



| <span data-ttu-id="40758-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="40758-116">Requirement</span></span> | <span data-ttu-id="40758-117">Valor</span><span class="sxs-lookup"><span data-stu-id="40758-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40758-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40758-118">Header</span></span><br/> | <dl> <span data-ttu-id="40758-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40758-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40758-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="40758-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40758-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="40758-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="40758-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="40758-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="40758-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="40758-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




