---
title: Mensagem de PSM_REBOOTSYSTEM (Prsht. h)
description: Indica que o sistema precisa ser reiniciado para que as alterações entrem em vigor. Você pode enviar a mensagem de PSM \_ REBOOTSYSTEM explicitamente ou usando a \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- Controles de PSM_REBOOTSYSTEM de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454927"
---
# <a name="psm_rebootsystem-message"></a><span data-ttu-id="99fc3-105">Mensagem de PSM \_ REBOOTSYSTEM</span><span class="sxs-lookup"><span data-stu-id="99fc3-105">PSM\_REBOOTSYSTEM message</span></span>

<span data-ttu-id="99fc3-106">Indica que o sistema precisa ser reiniciado para que as alterações entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="99fc3-106">Indicates the system needs to be restarted for the changes to take effect.</span></span> <span data-ttu-id="99fc3-107">Você pode enviar a mensagem de **PSM \_ REBOOTSYSTEM** explicitamente ou usando a macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .</span><span class="sxs-lookup"><span data-stu-id="99fc3-107">You can send the **PSM\_REBOOTSYSTEM** message explicitly or by using the [**PropSheet\_RebootSystem**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="99fc3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99fc3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99fc3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99fc3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="99fc3-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="99fc3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99fc3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99fc3-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="99fc3-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99fc3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99fc3-113">Return value</span></span>

<span data-ttu-id="99fc3-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="99fc3-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="99fc3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="99fc3-115">Remarks</span></span>

<span data-ttu-id="99fc3-116">Um aplicativo deve enviar essa mensagem somente em resposta à mensagem de notificação [PSN \_ Apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .</span><span class="sxs-lookup"><span data-stu-id="99fc3-116">An application should send this message only in response to the [PSN\_APPLY](psn-apply.md) or [PSN\_KILLACTIVE](psn-killactive.md) notification message.</span></span>

<span data-ttu-id="99fc3-117">Essa mensagem faz com que a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) retorne o \_ valor PSREBOOTSYSTEM da ID, mas somente se o usuário clicar no botão **OK** para fechar a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="99fc3-117">This message causes the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function to return the ID\_PSREBOOTSYSTEM value, but only if the user clicks the **OK** button to close the property sheet.</span></span> <span data-ttu-id="99fc3-118">É responsabilidade do aplicativo reinicializar o sistema, o que pode ser feito usando a função [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .</span><span class="sxs-lookup"><span data-stu-id="99fc3-118">It is the application's responsibility to reboot the system, which can be done by using the [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) function.</span></span>

<span data-ttu-id="99fc3-119">Essa mensagem substitui todas as mensagens de [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) que precedem ou seguem.</span><span class="sxs-lookup"><span data-stu-id="99fc3-119">This message supersedes all [**PSM\_RESTARTWINDOWS**](psm-restartwindows.md) messages that precede or follow it.</span></span>

> [!Note]  
> <span data-ttu-id="99fc3-120">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="99fc3-120">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99fc3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99fc3-121">Requirements</span></span>



| <span data-ttu-id="99fc3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="99fc3-122">Requirement</span></span> | <span data-ttu-id="99fc3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="99fc3-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99fc3-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99fc3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99fc3-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99fc3-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="99fc3-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99fc3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99fc3-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99fc3-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="99fc3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99fc3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99fc3-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="99fc3-129"><dt>Prsht.h</dt></span></span> </dl> |



 

