---
title: Mensagem de CB_SETCUEBANNER (WinUser. h)
description: Define o texto da faixa de indicação que é exibido para o controle de edição de uma caixa de combinação.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Controles de CB_SETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009354"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="e00b8-104">\_Mensagem de SETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="e00b8-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="e00b8-105">Define o texto da faixa de indicação que é exibido para o controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="e00b8-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="e00b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e00b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e00b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e00b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e00b8-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e00b8-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e00b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e00b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e00b8-110">Um ponteiro para um buffer de cadeia de caracteres Unicode terminada em nulo que contém o texto.</span><span class="sxs-lookup"><span data-stu-id="e00b8-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e00b8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e00b8-111">Return value</span></span>

<span data-ttu-id="e00b8-112">Retornará 1 se for bem-sucedido ou um valor de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e00b8-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e00b8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e00b8-113">Remarks</span></span>

<span data-ttu-id="e00b8-114">A faixa de indicação é o texto exibido no controle de edição de uma caixa de combinação quando não há seleção.</span><span class="sxs-lookup"><span data-stu-id="e00b8-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="e00b8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e00b8-115">Requirements</span></span>



| <span data-ttu-id="e00b8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e00b8-116">Requirement</span></span> | <span data-ttu-id="e00b8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e00b8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e00b8-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e00b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e00b8-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e00b8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e00b8-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e00b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e00b8-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e00b8-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e00b8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e00b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e00b8-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e00b8-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e00b8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e00b8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e00b8-125">Recursos da caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="e00b8-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





