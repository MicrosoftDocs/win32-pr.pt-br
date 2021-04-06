---
title: Mensagem de LVM_SORTGROUPS (commctrl. h)
description: Usa uma função de comparação definida pelo aplicativo para classificar grupos por ID dentro de um controle de exibição de lista.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Controles de LVM_SORTGROUPS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086149"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="a2edf-104">\_Mensagem SORTGROUPS LVM</span><span class="sxs-lookup"><span data-stu-id="a2edf-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="a2edf-105">Usa uma função de comparação definida pelo aplicativo para classificar grupos por ID dentro de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="a2edf-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2edf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2edf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2edf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a2edf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a2edf-108">Ponteiro para uma função de comparação definida pelo aplicativo, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span><span class="sxs-lookup"><span data-stu-id="a2edf-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="a2edf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2edf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a2edf-110">Ponteiro void para as informações definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2edf-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2edf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2edf-111">Return value</span></span>

<span data-ttu-id="a2edf-112">Retornará 1 se for bem-sucedido ou 0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a2edf-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2edf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2edf-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2edf-114">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="a2edf-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a2edf-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a2edf-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2edf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2edf-116">Requirements</span></span>



| <span data-ttu-id="a2edf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2edf-117">Requirement</span></span> | <span data-ttu-id="a2edf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a2edf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2edf-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2edf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2edf-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2edf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2edf-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2edf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2edf-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2edf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2edf-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2edf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2edf-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2edf-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2edf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2edf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2edf-126">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="a2edf-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

