---
title: Mensagem de TTM_UPDATETIPTEXT (commctrl. h)
description: Define o texto de ToolTip para uma ferramenta.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Controles de TTM_UPDATETIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085807"
---
# <a name="ttm_updatetiptext-message"></a><span data-ttu-id="2b795-104">\_Mensagem TTM UPDATETIPTEXT</span><span class="sxs-lookup"><span data-stu-id="2b795-104">TTM\_UPDATETIPTEXT message</span></span>

<span data-ttu-id="2b795-105">Define o texto de ToolTip para uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="2b795-105">Sets the tooltip text for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b795-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b795-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b795-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b795-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b795-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2b795-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b795-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b795-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="2b795-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="2b795-111">Os membros **hinst** e **lpszText** devem especificar o identificador de instância e o endereço do texto.</span><span class="sxs-lookup"><span data-stu-id="2b795-111">The **hinst** and **lpszText** members must specify the instance handle and the address of the text.</span></span> <span data-ttu-id="2b795-112">Os membros de **HWND** e **UID** identificam a ferramenta a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2b795-112">The **hwnd** and **uId** members identify the tool to update.</span></span> <span data-ttu-id="2b795-113">O membro **cbSize** dessa estrutura deve ser preenchido antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b795-113">The **cbSize** member of this structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b795-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b795-114">Return value</span></span>

<span data-ttu-id="2b795-115">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2b795-115">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b795-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b795-116">Requirements</span></span>



| <span data-ttu-id="2b795-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b795-117">Requirement</span></span> | <span data-ttu-id="2b795-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2b795-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b795-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b795-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2b795-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b795-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b795-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b795-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2b795-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b795-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b795-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b795-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b795-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b795-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2b795-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2b795-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2b795-126">**TTM \_ UPDATETIPTEXTW** (Unicode) e **TTM \_ UPDATETIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2b795-126">**TTM\_UPDATETIPTEXTW** (Unicode) and **TTM\_UPDATETIPTEXTA** (ANSI)</span></span><br/>       |



 

 





