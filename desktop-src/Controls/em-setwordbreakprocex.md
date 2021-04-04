---
title: Mensagem de EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Define o procedimento de quebra de palavra estendido para um controle de edição rico.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Controles de EM_SETWORDBREAKPROCEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918279"
---
# <a name="em_setwordbreakprocex-message"></a><span data-ttu-id="88331-104">\_Mensagem em SETWORDBREAKPROCEX</span><span class="sxs-lookup"><span data-stu-id="88331-104">EM\_SETWORDBREAKPROCEX message</span></span>

<span data-ttu-id="88331-105">Define o procedimento de quebra de palavra estendido para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="88331-105">Sets the extended word-break procedure for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="88331-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88331-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88331-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88331-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="88331-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="88331-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88331-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88331-110">Ponteiro para uma função [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) ou **nulo** para usar o procedimento padrão.</span><span class="sxs-lookup"><span data-stu-id="88331-110">Pointer to an [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) function, or **NULL** to use the default procedure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88331-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88331-111">Return value</span></span>

<span data-ttu-id="88331-112">Essa mensagem retorna o endereço do procedimento de quebra de palavra estendido anterior.</span><span class="sxs-lookup"><span data-stu-id="88331-112">This message returns the address of the previous extended word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="88331-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88331-113">Requirements</span></span>



| <span data-ttu-id="88331-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88331-114">Requirement</span></span> | <span data-ttu-id="88331-115">Valor</span><span class="sxs-lookup"><span data-stu-id="88331-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88331-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88331-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88331-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88331-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88331-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88331-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88331-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="88331-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88331-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88331-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88331-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="88331-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88331-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="88331-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="88331-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="88331-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88331-124">**EditWordBreakProcEx**</span><span class="sxs-lookup"><span data-stu-id="88331-124">**EditWordBreakProcEx**</span></span>](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[<span data-ttu-id="88331-125">**em \_ GETWORDBREAKPROCEX**</span><span class="sxs-lookup"><span data-stu-id="88331-125">**EM\_GETWORDBREAKPROCEX**</span></span>](em-getwordbreakprocex.md)
</dt> </dl>

 

 





