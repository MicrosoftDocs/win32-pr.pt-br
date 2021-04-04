---
title: Mensagem de TDM_CLICK_VERIFICATION (commctrl. h)
description: Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Controles de TDM_CLICK_VERIFICATION de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085149"
---
# <a name="tdm_click_verification-message"></a><span data-ttu-id="a0273-104">Mensagem de verificação de \_ clique de TDM \_</span><span class="sxs-lookup"><span data-stu-id="a0273-104">TDM\_CLICK\_VERIFICATION message</span></span>

<span data-ttu-id="a0273-105">Simula um clique da caixa de seleção de verificação de uma caixa de diálogo de tarefa, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="a0273-105">Simulates a click of the verification checkbox of a task dialog, if it exists.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0273-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0273-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0273-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0273-108">**True** para definir o estado da caixa de seleção como marcada; **False** para defini-lo como desmarcado.</span><span class="sxs-lookup"><span data-stu-id="a0273-108">**TRUE** to set the state of the checkbox to be checked; **FALSE** to set it to be unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="a0273-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0273-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0273-110">**True** para definir o foco do teclado para a caixa de seleção; Caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="a0273-110">**TRUE** to set the keyboard focus to the checkbox; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0273-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0273-111">Return value</span></span>

<span data-ttu-id="a0273-112">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="a0273-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0273-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0273-113">Requirements</span></span>



| <span data-ttu-id="a0273-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0273-114">Requirement</span></span> | <span data-ttu-id="a0273-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a0273-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0273-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0273-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0273-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0273-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0273-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0273-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0273-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0273-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0273-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0273-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0273-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0273-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





