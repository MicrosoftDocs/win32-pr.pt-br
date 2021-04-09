---
title: Mensagem de PSM_SETCURSELID (Prsht. h)
description: Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Controles de PSM_SETCURSELID de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086024"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="68928-105">Mensagem de PSM \_ SETCURSELID</span><span class="sxs-lookup"><span data-stu-id="68928-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="68928-106">Ativa a página determinada em uma folha de propriedades com base no identificador de recurso da página.</span><span class="sxs-lookup"><span data-stu-id="68928-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="68928-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .</span><span class="sxs-lookup"><span data-stu-id="68928-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68928-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68928-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68928-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68928-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68928-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="68928-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68928-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68928-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68928-112">Identificador de recurso da página a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="68928-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68928-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68928-113">Return value</span></span>

<span data-ttu-id="68928-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="68928-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="68928-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="68928-115">Remarks</span></span>

<span data-ttu-id="68928-116">A janela que está perdendo a ativação recebe o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) e a janela que está recebendo a ativação recebe o código de notificação [ \_ SetActive PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="68928-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68928-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68928-117">Requirements</span></span>



| <span data-ttu-id="68928-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68928-118">Requirement</span></span> | <span data-ttu-id="68928-119">Valor</span><span class="sxs-lookup"><span data-stu-id="68928-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68928-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68928-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68928-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68928-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68928-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68928-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68928-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68928-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68928-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68928-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68928-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="68928-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





