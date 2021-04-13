---
title: Mensagem de PSM_GETRESULT (Prsht. h)
description: Usado por folhas de propriedades sem janela restrita para recuperar as informações retornadas às folhas de propriedades modais por folha. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetResult PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Controles de PSM_GETRESULT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499625"
---
# <a name="psm_getresult-message"></a><span data-ttu-id="48fc3-105">Mensagem de PSM \_ GETresult</span><span class="sxs-lookup"><span data-stu-id="48fc3-105">PSM\_GETRESULT message</span></span>

<span data-ttu-id="48fc3-106">Usado por folhas de propriedades sem janela restrita para recuperar as informações retornadas às folhas de propriedades modais por [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span><span class="sxs-lookup"><span data-stu-id="48fc3-106">Used by modeless property sheets to retrieve the information returned to modal property sheets by [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta).</span></span> <span data-ttu-id="48fc3-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .</span><span class="sxs-lookup"><span data-stu-id="48fc3-107">You can send this message explicitly or use the [**PropSheet\_GetResult**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="48fc3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48fc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48fc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48fc3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="48fc3-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="48fc3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48fc3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48fc3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="48fc3-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48fc3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48fc3-113">Return value</span></span>

<span data-ttu-id="48fc3-114">Retorna um valor positivo se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="48fc3-114">Returns a positive value if successful, or -1 otherwise.</span></span> <span data-ttu-id="48fc3-115">Os valores de retorno a seguir têm um significado especial.</span><span class="sxs-lookup"><span data-stu-id="48fc3-115">The following return values have a special meaning.</span></span>



| <span data-ttu-id="48fc3-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48fc3-116">Return code</span></span>                                                                                         | <span data-ttu-id="48fc3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="48fc3-117">Description</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48fc3-118"><dt>**ID \_ PSREBOOTSYSTEM**</dt></span><span class="sxs-lookup"><span data-stu-id="48fc3-118"><dt>**ID\_PSREBOOTSYSTEM**</dt></span></span> </dl>   | <span data-ttu-id="48fc3-119">Uma página enviou uma mensagem de [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="48fc3-119">A page sent a [**PSM\_REBOOTSYSTEM**](psm-rebootsystem.md) message to the property sheet.</span></span> <span data-ttu-id="48fc3-120">O computador deve ser reiniciado para que as alterações do usuário entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="48fc3-120">The computer must be restarted for the user's changes to take effect.</span></span><br/> |
| <dl> <span data-ttu-id="48fc3-121"><dt>**ID \_ PSRESTARTWINDOWS**</dt></span><span class="sxs-lookup"><span data-stu-id="48fc3-121"><dt>**ID\_PSRESTARTWINDOWS**</dt></span></span> </dl> | <span data-ttu-id="48fc3-122">Uma página enviou uma mensagem de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="48fc3-122">A page sent a [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) message to the property sheet.</span></span> <span data-ttu-id="48fc3-123">O Windows deve ser reiniciado para que as alterações do usuário entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="48fc3-123">Windows must be restarted for the user's changes to take effect.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="48fc3-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="48fc3-124">Remarks</span></span>

<span data-ttu-id="48fc3-125">Para recuperar informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="48fc3-125">To retrieve extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

<span data-ttu-id="48fc3-126">O valor de retorno para essa mensagem é idêntico ao que [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorna para uma folha de propriedades modal.</span><span class="sxs-lookup"><span data-stu-id="48fc3-126">The return value for this message is identical to what [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) returns for a modal property sheet.</span></span>

[<span data-ttu-id="48fc3-127">Versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="48fc3-127">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="48fc3-128">O valor de retorno [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) transporta informações diferentes para folhas de propriedades modais e sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="48fc3-128">The [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) return value carries different information for modal and modeless property sheets.</span></span> <span data-ttu-id="48fc3-129">Em alguns casos, as folhas de propriedades sem janela restrita podem precisar das informações recebidas de **folha** se tivessem sido modais.</span><span class="sxs-lookup"><span data-stu-id="48fc3-129">In some cases, modeless property sheets may need the information they would have received from **PropertySheet** if they had been modal.</span></span> <span data-ttu-id="48fc3-130">Em particular, talvez seja necessário saber se a ID \_ PSREBOOTSYSTEM ou a ID \_ PSRESTARTWINDOWS teria sido retornada.</span><span class="sxs-lookup"><span data-stu-id="48fc3-130">In particular, they may need to know whether ID\_PSREBOOTSYSTEM or ID\_PSRESTARTWINDOWS would have been returned.</span></span>

<span data-ttu-id="48fc3-131">Para uma folha de propriedades sem janela restrita, o loop de mensagem deve usar o [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) para passar as mensagens para a caixa de diálogo da folha de propriedades e o [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) para determinar quando destruir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="48fc3-131">For a modeless property sheet, your message loop should use [**PSM\_ISDIALOGMESSAGE**](psm-isdialogmessage.md) to pass messages to the property sheet dialog box, and [**PSM\_GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) to determine when to destroy the dialog box.</span></span> <span data-ttu-id="48fc3-132">Quando o usuário clica no botão **OK** ou **Cancelar** , o **PSM \_ GETCURRENTPAGEHWND** retorna **nulo**.</span><span class="sxs-lookup"><span data-stu-id="48fc3-132">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**.</span></span> <span data-ttu-id="48fc3-133">Em seguida, você pode recuperar o valor que uma folha de propriedades modal teria recebido de [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) enviando uma mensagem de **PSM \_ GetResult** .</span><span class="sxs-lookup"><span data-stu-id="48fc3-133">You can then retrieve the value that a modal property sheet would have received from [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) by sending a **PSM\_GETRESULT** message.</span></span>

> [!Note]  
> <span data-ttu-id="48fc3-134">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="48fc3-134">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="48fc3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48fc3-135">Requirements</span></span>



| <span data-ttu-id="48fc3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="48fc3-136">Requirement</span></span> | <span data-ttu-id="48fc3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="48fc3-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48fc3-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fc3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="48fc3-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48fc3-139">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="48fc3-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48fc3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="48fc3-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48fc3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="48fc3-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48fc3-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="48fc3-143"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="48fc3-143"><dt>Prsht.h</dt></span></span> </dl> |



 

