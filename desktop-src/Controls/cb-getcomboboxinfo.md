---
title: Mensagem de CB_GETCOMBOBOXINFO (WinUser. h)
description: Obtém informações sobre a caixa de combinação especificada.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- Controles de CB_GETCOMBOBOXINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454710"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="dd373-104">\_Mensagem de GETCOMBOBOXINFO CB</span><span class="sxs-lookup"><span data-stu-id="dd373-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="dd373-105">Obtém informações sobre a caixa de combinação especificada.</span><span class="sxs-lookup"><span data-stu-id="dd373-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd373-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd373-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd373-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd373-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="dd373-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd373-109">*lParam* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dd373-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd373-110">Um ponteiro para uma estrutura [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) que recebe as informações.</span><span class="sxs-lookup"><span data-stu-id="dd373-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd373-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dd373-111">Return value</span></span>

<span data-ttu-id="dd373-112">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="dd373-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="dd373-113">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="dd373-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="dd373-114">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="dd373-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd373-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd373-115">Remarks</span></span>

<span data-ttu-id="dd373-116">Essa mensagem é equivalente a [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="dd373-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd373-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd373-117">Requirements</span></span>



| <span data-ttu-id="dd373-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd373-118">Requirement</span></span> | <span data-ttu-id="dd373-119">Valor</span><span class="sxs-lookup"><span data-stu-id="dd373-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd373-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd373-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd373-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd373-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dd373-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd373-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd373-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd373-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dd373-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd373-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd373-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd373-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd373-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd373-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd373-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dd373-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd373-128">**COMBOBOXINFO**</span><span class="sxs-lookup"><span data-stu-id="dd373-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="dd373-129">**GetComboBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="dd373-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

