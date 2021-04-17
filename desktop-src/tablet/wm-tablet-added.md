---
description: A mensagem do WM \_ Tablet \_ adicionado é postada quando um dispositivo de Tablet é adicionado ao Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Mensagem de WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811451"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="19578-103">Mensagem do WM \_ Tablet \_ adicionado</span><span class="sxs-lookup"><span data-stu-id="19578-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="19578-104">A mensagem do **WM \_ Tablet \_ adicionado** é postada quando um dispositivo de Tablet é adicionado ao Windows.</span><span class="sxs-lookup"><span data-stu-id="19578-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="19578-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19578-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19578-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19578-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19578-107">Índice do dispositivo do Tablet que está sendo adicionado</span><span class="sxs-lookup"><span data-stu-id="19578-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="19578-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19578-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19578-109">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="19578-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19578-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="19578-110">Remarks</span></span>

<span data-ttu-id="19578-111">Essa mensagem é enviada para todas as janelas de nível superior no sistema, incluindo janelas desativas ou invisíveis, janelas e janelas pop-up sem proprietário. Mas a mensagem não é enviada para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="19578-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="19578-112">Os índices passados em *wParam* estão relacionados ao índice usado pelo método [**ITabletManager:: getTableName**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19578-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="19578-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19578-113">Requirements</span></span>



| <span data-ttu-id="19578-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="19578-114">Requirement</span></span> | <span data-ttu-id="19578-115">Valor</span><span class="sxs-lookup"><span data-stu-id="19578-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19578-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19578-116">Minimum supported client</span></span><br/> | <span data-ttu-id="19578-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="19578-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="19578-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19578-118">Minimum supported server</span></span><br/> | <span data-ttu-id="19578-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19578-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="19578-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19578-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="19578-121"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="19578-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
