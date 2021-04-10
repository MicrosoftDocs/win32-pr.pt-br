---
title: Mensagem de CCM_SETVERSION (commctrl. h)
description: Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Controles de CCM_SETVERSION de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009530"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="de009-104">\_Mensagem CCM SETversion</span><span class="sxs-lookup"><span data-stu-id="de009-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="de009-105">Essa mensagem é usada para informar o controle de que você está esperando um comportamento associado a uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="de009-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="de009-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de009-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de009-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de009-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de009-108">O número de versão.</span><span class="sxs-lookup"><span data-stu-id="de009-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="de009-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de009-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de009-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="de009-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de009-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de009-111">Return value</span></span>

<span data-ttu-id="de009-112">Retorna a versão especificada na mensagem **CCM \_ SetVersion** anterior.</span><span class="sxs-lookup"><span data-stu-id="de009-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="de009-113">Se *wParam* for definido como um valor maior que a versão atual da dll, ele retornará-1.</span><span class="sxs-lookup"><span data-stu-id="de009-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="de009-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="de009-114">Remarks</span></span>

<span data-ttu-id="de009-115">Em alguns casos, um controle pode se comportar de forma diferente, dependendo da versão.</span><span class="sxs-lookup"><span data-stu-id="de009-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="de009-116">Isso se aplica principalmente a bugs que foram corrigidos em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="de009-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="de009-117">A mensagem **CCM \_ SetVersion** permite informar ao controle qual comportamento é esperado.</span><span class="sxs-lookup"><span data-stu-id="de009-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="de009-118">Você pode determinar qual versão você especificou enviando uma mensagem [**CCM \_ GetVersion**](ccm-getversion.md) .</span><span class="sxs-lookup"><span data-stu-id="de009-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="de009-119">Para obter um exemplo de como usar essa mensagem, consulte [desenho personalizado com List-View e controles de Tree-View](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="de009-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="de009-120">Se você tiver ComCtl32.dll versão 6 instalada, independentemente do valor que você definiu em *wParam*, a mensagem **CCM \_ SetVersion** retornará a versão 6.</span><span class="sxs-lookup"><span data-stu-id="de009-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="de009-121">Essa mensagem define apenas o número de versão do controle para o qual ele é enviado.</span><span class="sxs-lookup"><span data-stu-id="de009-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de009-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de009-122">Requirements</span></span>



| <span data-ttu-id="de009-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="de009-123">Requirement</span></span> | <span data-ttu-id="de009-124">Valor</span><span class="sxs-lookup"><span data-stu-id="de009-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de009-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de009-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de009-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de009-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de009-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de009-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de009-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="de009-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de009-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de009-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="de009-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="de009-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





