---
title: Mensagem de EM_HIDESELECTION (RichEdit. h)
description: A \_ mensagem em HIDESELECTION oculta ou mostra a seleção em um controle de edição rico.
ms.assetid: 1245618f-c9e6-4876-9133-6009370cdb97
keywords:
- Controles de EM_HIDESELECTION de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_HIDESELECTION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a5690e52c2a25f5a359de205ac1584e1ef45ed4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918061"
---
# <a name="em_hideselection-message"></a><span data-ttu-id="36f24-104">\_Mensagem em HIDESELECTION</span><span class="sxs-lookup"><span data-stu-id="36f24-104">EM\_HIDESELECTION message</span></span>

<span data-ttu-id="36f24-105">A mensagem em **\_ HIDESELECTION** oculta ou mostra a seleção em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="36f24-105">The **EM\_HIDESELECTION** message hides or shows the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="36f24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36f24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f24-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36f24-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36f24-108">Valor que especifica se a seleção deve ser ocultada ou mostrada.</span><span class="sxs-lookup"><span data-stu-id="36f24-108">Value specifying whether to hide or show the selection.</span></span> <span data-ttu-id="36f24-109">Se esse parâmetro for zero, a seleção será mostrada.</span><span class="sxs-lookup"><span data-stu-id="36f24-109">If this parameter is zero, the selection is shown.</span></span> <span data-ttu-id="36f24-110">Caso contrário, a seleção ficará oculta.</span><span class="sxs-lookup"><span data-stu-id="36f24-110">Otherwise, the selection is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="36f24-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36f24-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36f24-112">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="36f24-112">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f24-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36f24-113">Return value</span></span>

<span data-ttu-id="36f24-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="36f24-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f24-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f24-115">Requirements</span></span>



| <span data-ttu-id="36f24-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f24-116">Requirement</span></span> | <span data-ttu-id="36f24-117">Valor</span><span class="sxs-lookup"><span data-stu-id="36f24-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36f24-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36f24-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36f24-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36f24-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36f24-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36f24-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36f24-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36f24-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36f24-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36f24-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36f24-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f24-123"><dt>Richedit.h</dt></span></span> </dl> |



 

 





