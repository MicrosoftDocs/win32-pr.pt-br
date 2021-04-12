---
title: Mensagem de LVM_SETGROUPMETRICS (commctrl. h)
description: Define informações sobre a exibição de grupos.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- Controles de LVM_SETGROUPMETRICS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294754"
---
# <a name="lvm_setgroupmetrics-message"></a><span data-ttu-id="6ec9d-104">\_Mensagem SETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="6ec9d-104">LVM\_SETGROUPMETRICS message</span></span>

<span data-ttu-id="6ec9d-105">Define informações sobre a exibição de grupos.</span><span class="sxs-lookup"><span data-stu-id="6ec9d-105">Sets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ec9d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ec9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec9d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ec9d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ec9d-108">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6ec9d-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="6ec9d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ec9d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ec9d-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que contém as métricas a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="6ec9d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that contains the metrics to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec9d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ec9d-111">Return value</span></span>

<span data-ttu-id="6ec9d-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="6ec9d-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec9d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ec9d-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ec9d-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6ec9d-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6ec9d-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ec9d-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ec9d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec9d-116">Requirements</span></span>



| <span data-ttu-id="6ec9d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec9d-117">Requirement</span></span> | <span data-ttu-id="6ec9d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ec9d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec9d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec9d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec9d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ec9d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ec9d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec9d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec9d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ec9d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ec9d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ec9d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec9d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec9d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





