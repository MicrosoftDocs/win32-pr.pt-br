---
description: A \_ \_ mensagem excluída do WM Tablet é postada quando um dispositivo tablet é removido do Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Mensagem de WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781156"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="486a2-103">\_ \_ Mensagem excluída do WM Tablet</span><span class="sxs-lookup"><span data-stu-id="486a2-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="486a2-104">A **mensagem \_ \_ excluída do WM Tablet** é postada quando um dispositivo tablet é removido do Windows.</span><span class="sxs-lookup"><span data-stu-id="486a2-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="486a2-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="486a2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="486a2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="486a2-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="486a2-107">Índice do dispositivo tablet que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="486a2-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="486a2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="486a2-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="486a2-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="486a2-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="486a2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="486a2-110">Remarks</span></span>

<span data-ttu-id="486a2-111">Essa mensagem é enviada para todas as janelas de nível superior no sistema, incluindo janelas desativas ou invisíveis, janelas e janelas pop-up sem proprietário. Mas a mensagem não é enviada para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="486a2-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="486a2-112">Os índices passados em *wParam* estão relacionados ao índice usado pelo método [**ITabletManager:: getTableName**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="486a2-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="486a2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="486a2-113">Requirements</span></span>



| <span data-ttu-id="486a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="486a2-114">Requirement</span></span> | <span data-ttu-id="486a2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="486a2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="486a2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="486a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="486a2-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="486a2-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="486a2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="486a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="486a2-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="486a2-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="486a2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="486a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="486a2-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="486a2-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
