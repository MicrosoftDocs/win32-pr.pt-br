---
title: Mensagem de LVM_INSERTGROUPSORTED (commctrl. h)
description: Insere um grupo em uma lista ordenada de grupos.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Controles de LVM_INSERTGROUPSORTED de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824663"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="05f32-104">\_Mensagem INSERTGROUPSORTED LVM</span><span class="sxs-lookup"><span data-stu-id="05f32-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="05f32-105">Insere um grupo em uma lista ordenada de grupos.</span><span class="sxs-lookup"><span data-stu-id="05f32-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="05f32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05f32-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="05f32-108">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> que contém o grupo a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="05f32-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="05f32-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05f32-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="05f32-110">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="05f32-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f32-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05f32-111">Return value</span></span>

<span data-ttu-id="05f32-112">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="05f32-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f32-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="05f32-113">Remarks</span></span>

<span data-ttu-id="05f32-114">A ordenação da lista é baseada na ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="05f32-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="05f32-115">A ordem é definida pela função de ordenação definida pelo aplicativo, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), que é passada na estrutura [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="05f32-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="05f32-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="05f32-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="05f32-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="05f32-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05f32-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f32-118">Requirements</span></span>



| <span data-ttu-id="05f32-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f32-119">Requirement</span></span> | <span data-ttu-id="05f32-120">Valor</span><span class="sxs-lookup"><span data-stu-id="05f32-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05f32-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05f32-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05f32-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05f32-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05f32-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05f32-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05f32-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="05f32-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05f32-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05f32-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f32-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f32-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f32-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="05f32-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="05f32-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="05f32-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05f32-129">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="05f32-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="05f32-130">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="05f32-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

