---
title: Mensagem de PSM_SETCURSEL (Prsht. h)
description: Ativa a página especificada em uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Setcurseal PropSheet.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Controles de PSM_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085458"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="63353-105">Mensagem de PSM \_ SETcurse</span><span class="sxs-lookup"><span data-stu-id="63353-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="63353-106">Ativa a página especificada em uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="63353-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="63353-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ setcurseal PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="63353-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="63353-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63353-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63353-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63353-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63353-110">O índice de base zero da página.</span><span class="sxs-lookup"><span data-stu-id="63353-110">The zero-based index of the page.</span></span> <span data-ttu-id="63353-111">Um aplicativo pode especificar o índice ou o identificador ou ambos.</span><span class="sxs-lookup"><span data-stu-id="63353-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="63353-112">Se ambos forem especificados, *lParam* terá precedência.</span><span class="sxs-lookup"><span data-stu-id="63353-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="63353-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63353-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63353-114">O identificador da página a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="63353-114">The handle to the page to activate.</span></span> <span data-ttu-id="63353-115">Um aplicativo pode especificar o índice ou o identificador ou ambos.</span><span class="sxs-lookup"><span data-stu-id="63353-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="63353-116">Se ambos forem especificados, *lParam* terá precedência.</span><span class="sxs-lookup"><span data-stu-id="63353-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63353-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63353-117">Return value</span></span>

<span data-ttu-id="63353-118">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="63353-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="63353-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="63353-119">Remarks</span></span>

<span data-ttu-id="63353-120">A janela que está perdendo a ativação recebe o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) e a janela que está recebendo a ativação recebe o código de notificação [ \_ SetActive PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="63353-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="63353-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63353-121">Requirements</span></span>



| <span data-ttu-id="63353-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63353-122">Requirement</span></span> | <span data-ttu-id="63353-123">Valor</span><span class="sxs-lookup"><span data-stu-id="63353-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63353-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63353-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63353-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63353-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63353-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63353-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63353-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63353-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63353-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63353-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="63353-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="63353-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





