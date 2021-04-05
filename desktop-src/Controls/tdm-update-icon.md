---
title: Mensagem de TDM_UPDATE_ICON (commctrl. h)
description: Atualiza o ícone de uma caixa de diálogo de tarefa.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- Controles de TDM_UPDATE_ICON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919165"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="9fee1-104">Mensagem de ícone de \_ atualização TDM \_</span><span class="sxs-lookup"><span data-stu-id="9fee1-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="9fee1-105">Atualiza o ícone de uma caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="9fee1-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fee1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fee1-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fee1-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fee1-108">Indica qual elemento de ícone deve ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9fee1-108">Indicates which icon element to update.</span></span> <span data-ttu-id="9fee1-109">Esse parâmetro deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="9fee1-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="9fee1-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9fee1-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="9fee1-111">Significado</span><span class="sxs-lookup"><span data-stu-id="9fee1-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="9fee1-112"><dt>**TDIE \_ ícone \_ principal**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="9fee1-113">Ícone principal.</span><span class="sxs-lookup"><span data-stu-id="9fee1-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="9fee1-114"><dt>**\_rodapé do ícone de TDIE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="9fee1-115">Ícone de rodapé.</span><span class="sxs-lookup"><span data-stu-id="9fee1-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9fee1-116">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9fee1-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fee1-117">Um ponteiro para uma cadeia de caracteres (PCWSTR) ou um identificador para um ícone (HICON) a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="9fee1-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="9fee1-118">Se *lParam* for **nulo**, nenhum ícone será exibido, independentemente do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="9fee1-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="9fee1-119">Se o valor de *wParam* for TDIE \_ ícone \_ principal e TDF \_ usar \_ HICON \_ sinalizador principal estiver definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa, *lParam* deverá conter um identificador para um ícone (HICON) a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="9fee1-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="9fee1-120">Se o valor de *wParam* é um \_ rodapé de ícone TDIE \_ e \_ o \_ sinalizador de rodapé usar HICON TDF \_ é definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa, *lParam* deve conter um identificador para um ícone (HICON) a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="9fee1-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="9fee1-121">Se o TDF \_ usar \_ HICON \_ Main ou TDF \_ use \_ HICON \_ sinalizadores de rodapé **não** estiverem definidos no membro **dwFlags** , *lParam* deverá apontar para uma cadeia de caracteres Unicode terminada com NULL (PCWSTR) que contenha um identificador de recurso válido passado pela macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="9fee1-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="9fee1-122">O ícone é exibido com base no valor de *wParam*: se o valor for TDIE \_ ícone \_ principal, o ícone será exibido no cabeçalho; se o valor for TDIE \_ ícone \_ rodapé, o ícone será exibido no rodapé.</span><span class="sxs-lookup"><span data-stu-id="9fee1-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="9fee1-123">O recurso deve ser do módulo de recurso do aplicativo (especificado no membro **HINSTANCE** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) ou, se **HINSTANCE** for **NULL**, do módulo de recurso do sistema (imageres.dll).</span><span class="sxs-lookup"><span data-stu-id="9fee1-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="9fee1-124">Para identificar um recurso do sistema, use um identificador de sistema válido passado pela macro **MAKEINTRESOURCE** ou um dos seguintes valores predefinidos de commctrl. h:</span><span class="sxs-lookup"><span data-stu-id="9fee1-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="9fee1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9fee1-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="9fee1-126">Significado</span><span class="sxs-lookup"><span data-stu-id="9fee1-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="9fee1-127"><dt>**\_ícone de erro TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="9fee1-128">Um ícone de sinal de parada.</span><span class="sxs-lookup"><span data-stu-id="9fee1-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="9fee1-129"><dt>**\_ícone de aviso TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="9fee1-130">Um ícone de ponto de exclamação.</span><span class="sxs-lookup"><span data-stu-id="9fee1-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="9fee1-131"><dt>**\_ícone de informações TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="9fee1-132">Uma letra minúscula "i" em um ícone de círculo.</span><span class="sxs-lookup"><span data-stu-id="9fee1-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="9fee1-133"><dt>**\_ícone de escudo TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="9fee1-134">Um ícone de escudo de segurança.</span><span class="sxs-lookup"><span data-stu-id="9fee1-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fee1-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9fee1-135">Return value</span></span>

<span data-ttu-id="9fee1-136">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="9fee1-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fee1-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fee1-137">Remarks</span></span>

<span data-ttu-id="9fee1-138">O layout da caixa de diálogo de tarefa com o ícone pode falhar e isso pode não ser refletido no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="9fee1-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="9fee1-139">Um valor de retorno de S \_ OK reflete apenas que a caixa de diálogo de tarefa recebeu a mensagem e tentou processá-la.</span><span class="sxs-lookup"><span data-stu-id="9fee1-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="9fee1-140">Se o layout da caixa de diálogo de tarefa falhar, a caixa de diálogo será fechada e um código **HRESULT** será retornado na função de retorno de chamada registrada.</span><span class="sxs-lookup"><span data-stu-id="9fee1-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="9fee1-141">Para obter mais informações sobre a sintaxe da função de retorno de chamada, consulte [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="9fee1-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="9fee1-142">Se a caixa de diálogo de tarefa for criada sem um rodapé (ou seja, os membros de rodapé apropriados da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usados para criar a caixa de diálogo de tarefa serão **nulos**) e essa mensagem será enviada, um rodapé não será adicionado dinamicamente à caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="9fee1-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="9fee1-143">O mesmo é verdadeiro para enviar essa mensagem para atualizar um ícone de cabeçalho quando uma caixa de diálogo de tarefa é criada sem um cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="9fee1-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="9fee1-144">Para adicionar um cabeçalho ou rodapé em tempo de execução, use a funcionalidade de [**\_ \_ página de navegação TDM**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="9fee1-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fee1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fee1-145">Requirements</span></span>



| <span data-ttu-id="9fee1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fee1-146">Requirement</span></span> | <span data-ttu-id="9fee1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="9fee1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fee1-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fee1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9fee1-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fee1-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fee1-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9fee1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9fee1-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fee1-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fee1-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9fee1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fee1-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fee1-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

