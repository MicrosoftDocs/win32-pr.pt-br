---
title: Mensagem de BCM_GETNOTELENGTH (commctrl. h)
description: Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando. Envie essa mensagem explicitamente ou usando o botão \_ GetNoteLength macro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Controles de BCM_GETNOTELENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009271"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="61311-105">\_Mensagem GETNOTELENGTH do BCM</span><span class="sxs-lookup"><span data-stu-id="61311-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="61311-106">Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando.</span><span class="sxs-lookup"><span data-stu-id="61311-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="61311-107">Envie essa mensagem explicitamente ou usando o [**botão \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span><span class="sxs-lookup"><span data-stu-id="61311-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61311-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61311-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61311-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61311-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61311-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="61311-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="61311-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61311-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61311-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="61311-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61311-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61311-113">Return value</span></span>

<span data-ttu-id="61311-114">Retorna o comprimento do texto da nota em **WCHARs**, não incluindo nenhum **nulo** de término ou zero se não houver texto de nota.</span><span class="sxs-lookup"><span data-stu-id="61311-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="61311-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61311-115">Remarks</span></span>

<span data-ttu-id="61311-116">Começando com o comctl32 DLL versão 6, 1, os botões de link de comando podem ter uma observação.</span><span class="sxs-lookup"><span data-stu-id="61311-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="61311-117">Para obter informações sobre versões de DLL, consulte [versões de controle comuns](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="61311-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="61311-118">A **mensagem \_ GETNOTELENGTH do BCM** funciona apenas com os estilos de botão [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="61311-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="61311-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61311-119">Requirements</span></span>



| <span data-ttu-id="61311-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="61311-120">Requirement</span></span> | <span data-ttu-id="61311-121">Valor</span><span class="sxs-lookup"><span data-stu-id="61311-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61311-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61311-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61311-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61311-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61311-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61311-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61311-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61311-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61311-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61311-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="61311-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61311-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61311-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="61311-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="61311-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="61311-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61311-130">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="61311-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="61311-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="61311-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61311-132">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="61311-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





