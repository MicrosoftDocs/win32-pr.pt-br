---
title: Mensagem de BCM_SETNOTE (commctrl. h)
description: Define o texto da observação associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a \_ macro setnote do botão.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Controles de BCM_SETNOTE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918437"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="4e2a3-105">Mensagem do BCM \_ SETnote</span><span class="sxs-lookup"><span data-stu-id="4e2a3-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="4e2a3-106">Define o texto da observação associada a um botão de link de comando.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="4e2a3-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ setnote do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .</span><span class="sxs-lookup"><span data-stu-id="4e2a3-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e2a3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e2a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e2a3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e2a3-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4e2a3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e2a3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e2a3-112">Um ponteiro para uma cadeia de caracteres **WCHAR** terminada em nulo que contém a observação.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2a3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e2a3-113">Return value</span></span>

<span data-ttu-id="4e2a3-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2a3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e2a3-115">Remarks</span></span>

<span data-ttu-id="4e2a3-116">Começando com o comctl32 DLL versão 6, 1, os botões de link de comando podem ter uma observação.</span><span class="sxs-lookup"><span data-stu-id="4e2a3-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="4e2a3-117">A mensagem de **\_ Observação do BCM** funciona apenas com os estilos de botão [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2a3-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2a3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e2a3-118">Requirements</span></span>



| <span data-ttu-id="4e2a3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2a3-119">Requirement</span></span> | <span data-ttu-id="4e2a3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4e2a3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2a3-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2a3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2a3-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e2a3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e2a3-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2a3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2a3-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e2a3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e2a3-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e2a3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2a3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2a3-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e2a3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e2a3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e2a3-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4e2a3-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e2a3-129">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="4e2a3-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="4e2a3-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4e2a3-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4e2a3-131">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="4e2a3-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





