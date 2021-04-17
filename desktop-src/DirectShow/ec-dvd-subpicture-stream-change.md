---
description: Sinaliza que o número de fluxo da subimagem atual foi alterado para o título principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759501"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="4b90f-103">\_alteração de \_ fluxo de subimagem do DVD do \_ EC \_</span><span class="sxs-lookup"><span data-stu-id="4b90f-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="4b90f-104">Sinaliza que o número de fluxo da subimagem atual foi alterado para o título principal.</span><span class="sxs-lookup"><span data-stu-id="4b90f-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b90f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b90f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b90f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4b90f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4b90f-107">Valor **DWORD** que indica o novo número de fluxo da subimagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b90f-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="4b90f-108">Os números de fluxo de subimagem variam de 0 a 31.</span><span class="sxs-lookup"><span data-stu-id="4b90f-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="4b90f-109">O fluxo 0xFFFFFFFF indica que nenhum fluxo está selecionado.</span><span class="sxs-lookup"><span data-stu-id="4b90f-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="4b90f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4b90f-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4b90f-111">Valor booliano que indica o estado ligado/desligado da subimagem.</span><span class="sxs-lookup"><span data-stu-id="4b90f-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b90f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b90f-112">Remarks</span></span>

<span data-ttu-id="4b90f-113">A subimagem pode ser alterada automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span><span class="sxs-lookup"><span data-stu-id="4b90f-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="4b90f-114">Esse evento é gerado em todos os domínios.</span><span class="sxs-lookup"><span data-stu-id="4b90f-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b90f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b90f-115">Requirements</span></span>



| <span data-ttu-id="4b90f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b90f-116">Requirement</span></span> | <span data-ttu-id="4b90f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4b90f-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b90f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b90f-118">Header</span></span><br/> | <dl> <span data-ttu-id="4b90f-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b90f-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b90f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b90f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b90f-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="4b90f-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="4b90f-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="4b90f-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4b90f-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4b90f-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




