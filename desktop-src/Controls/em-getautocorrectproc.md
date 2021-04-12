---
title: Mensagem de EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Obtém um ponteiro para a função AutoCorrectProc definida pelo aplicativo.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- Controles de EM_GETAUTOCORRECTPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455279"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="f55c7-104">\_Mensagem em GETAUTOCORRECTPROC</span><span class="sxs-lookup"><span data-stu-id="f55c7-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="f55c7-105">Obtém um ponteiro para a função [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f55c7-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="f55c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f55c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f55c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f55c7-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f55c7-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f55c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f55c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f55c7-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f55c7-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55c7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f55c7-111">Return value</span></span>

<span data-ttu-id="f55c7-112">Retorna um ponteiro para a função [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f55c7-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55c7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f55c7-113">Requirements</span></span>



| <span data-ttu-id="f55c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f55c7-114">Requirement</span></span> | <span data-ttu-id="f55c7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f55c7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f55c7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f55c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f55c7-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f55c7-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f55c7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f55c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f55c7-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f55c7-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f55c7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f55c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55c7-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55c7-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f55c7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f55c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55c7-123">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="f55c7-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="f55c7-124">**em \_ CALLAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="f55c7-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="f55c7-125">**em \_ SETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="f55c7-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





