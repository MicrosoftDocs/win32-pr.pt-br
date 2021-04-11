---
title: Mensagem de HKM_GETHOTKEY (commctrl. h)
description: Obtém o código de chave virtual e os sinalizadores de modificador de uma tecla de acesso de um controle de tecla de atalho.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Controles de HKM_GETHOTKEY de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455014"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="f8bd7-104">\_Mensagem hkm GETtecla de atalho</span><span class="sxs-lookup"><span data-stu-id="f8bd7-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="f8bd7-105">Obtém o código de chave virtual e os sinalizadores de modificador de uma tecla de acesso de um controle de tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8bd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8bd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8bd7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8bd7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8bd7-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8bd7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8bd7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f8bd7-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8bd7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8bd7-111">Return value</span></span>

<span data-ttu-id="f8bd7-112">Retorna o código de chave virtual e os sinalizadores de modificador.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="f8bd7-113">O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o código de chave virtual da tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="f8bd7-114">O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** é o modificador de chave que especifica as chaves que definem uma combinação de teclas de acesso.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="f8bd7-115">Os sinalizadores de modificadores podem ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8bd7-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="f8bd7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f8bd7-116">Value</span></span>            | <span data-ttu-id="f8bd7-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f8bd7-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="f8bd7-118">\_ALT HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="f8bd7-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="f8bd7-119">tecla ALT</span><span class="sxs-lookup"><span data-stu-id="f8bd7-119">ALT key</span></span>      |
| <span data-ttu-id="f8bd7-120">\_controle HOTKEYF</span><span class="sxs-lookup"><span data-stu-id="f8bd7-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="f8bd7-121">Chave de controle</span><span class="sxs-lookup"><span data-stu-id="f8bd7-121">CONTROL key</span></span>  |
| <span data-ttu-id="f8bd7-122">HOTKEYF \_ ext</span><span class="sxs-lookup"><span data-stu-id="f8bd7-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="f8bd7-123">Chave estendida</span><span class="sxs-lookup"><span data-stu-id="f8bd7-123">Extended key</span></span> |
| <span data-ttu-id="f8bd7-124">HOTKEYF \_ Shift</span><span class="sxs-lookup"><span data-stu-id="f8bd7-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="f8bd7-125">Tecla SHIFT</span><span class="sxs-lookup"><span data-stu-id="f8bd7-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="f8bd7-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8bd7-126">Remarks</span></span>

<span data-ttu-id="f8bd7-127">O valor de 16 bits retornado por essa mensagem pode ser usado como o parâmetro *wParam* na mensagem do [**WM \_ settecla**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="f8bd7-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bd7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8bd7-128">Requirements</span></span>



| <span data-ttu-id="f8bd7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8bd7-129">Requirement</span></span> | <span data-ttu-id="f8bd7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f8bd7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bd7-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8bd7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bd7-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8bd7-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8bd7-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8bd7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bd7-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8bd7-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8bd7-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8bd7-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8bd7-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8bd7-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

