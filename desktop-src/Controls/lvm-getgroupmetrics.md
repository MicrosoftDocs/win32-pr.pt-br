---
title: Mensagem de LVM_GETGROUPMETRICS (commctrl. h)
description: Obtém informações sobre a exibição de grupos.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- Controles de LVM_GETGROUPMETRICS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5af8ec50fe74ab90a0f3e44a69e2cbc7dda583e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918975"
---
# <a name="lvm_getgroupmetrics-message"></a><span data-ttu-id="d636c-104">\_Mensagem GETGROUPMETRICS LVM</span><span class="sxs-lookup"><span data-stu-id="d636c-104">LVM\_GETGROUPMETRICS message</span></span>

<span data-ttu-id="d636c-105">Obtém informações sobre a exibição de grupos.</span><span class="sxs-lookup"><span data-stu-id="d636c-105">Gets information about the display of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="d636c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d636c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d636c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d636c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d636c-108">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d636c-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="d636c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d636c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d636c-110">Um ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> que recebe as métricas recuperadas.</span><span class="sxs-lookup"><span data-stu-id="d636c-110">A pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS**</a> structure that receives the retrieved metrics.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d636c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d636c-111">Return value</span></span>

<span data-ttu-id="d636c-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="d636c-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d636c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d636c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d636c-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="d636c-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d636c-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d636c-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d636c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d636c-116">Requirements</span></span>



| <span data-ttu-id="d636c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d636c-117">Requirement</span></span> | <span data-ttu-id="d636c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d636c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d636c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d636c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d636c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d636c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d636c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d636c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d636c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d636c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d636c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d636c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d636c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d636c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





