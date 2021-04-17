---
description: Indica se um bloco de ângulo está sendo reproduzido e se as alterações de ângulo podem ser executadas.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783392"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="e4ae6-103">ângulos de DVD do EC \_ \_ \_ disponíveis</span><span class="sxs-lookup"><span data-stu-id="e4ae6-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="e4ae6-104">Indica se um bloco de ângulo está sendo reproduzido e se as alterações de ângulo podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="e4ae6-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4ae6-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4ae6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ae6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e4ae6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e4ae6-107">Valor booliano (**bool**) que indica se um bloco de ângulo está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="e4ae6-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="e4ae6-108">Zero (0) indica que a reprodução não está em um bloco de ângulo e os ângulos não estão disponíveis, um (1) indica que um bloco de ângulo está sendo reproduzido e alterações de ângulo podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="e4ae6-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="e4ae6-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e4ae6-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e4ae6-110">Zero.</span><span class="sxs-lookup"><span data-stu-id="e4ae6-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4ae6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4ae6-111">Remarks</span></span>

<span data-ttu-id="e4ae6-112">As alterações de ângulo não são restritas a blocos de ângulo e a manifestação da alteração de ângulo pode ser vista apenas em um bloco de ângulo.</span><span class="sxs-lookup"><span data-stu-id="e4ae6-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ae6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4ae6-113">Requirements</span></span>



| <span data-ttu-id="e4ae6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4ae6-114">Requirement</span></span> | <span data-ttu-id="e4ae6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e4ae6-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ae6-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4ae6-116">Header</span></span><br/> | <dl> <span data-ttu-id="e4ae6-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ae6-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4ae6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4ae6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ae6-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="e4ae6-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="e4ae6-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="e4ae6-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e4ae6-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4ae6-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




