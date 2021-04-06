---
title: Mensagem de LVM_GETFOOTERINFO (commctrl. h)
description: Obtém informações sobre o rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterInfo do ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Controles de LVM_GETFOOTERINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917996"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="b0046-105">\_Mensagem GETFOOTERINFO LVM</span><span class="sxs-lookup"><span data-stu-id="b0046-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="b0046-106">Obtém informações sobre o rodapé de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="b0046-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="b0046-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .</span><span class="sxs-lookup"><span data-stu-id="b0046-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0046-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0046-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0046-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0046-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0046-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="b0046-110">Not used.</span></span> <span data-ttu-id="b0046-111">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="b0046-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="b0046-112">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b0046-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0046-113">Um ponteiro para uma estrutura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) para receber informações dependendo do valor do membro **Mask** .</span><span class="sxs-lookup"><span data-stu-id="b0046-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="b0046-114">O processo de chamada é responsável por alocar essa estrutura e definir o membro de **máscara** .</span><span class="sxs-lookup"><span data-stu-id="b0046-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0046-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0046-115">Return value</span></span>

<span data-ttu-id="b0046-116">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="b0046-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0046-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0046-117">Requirements</span></span>



| <span data-ttu-id="b0046-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0046-118">Requirement</span></span> | <span data-ttu-id="b0046-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b0046-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0046-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0046-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0046-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0046-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0046-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0046-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0046-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0046-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0046-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0046-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0046-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0046-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





