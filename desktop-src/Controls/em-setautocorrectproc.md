---
title: Mensagem de EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Define o procedimento de retorno de chamada da AutoCorreção atual.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Controles de EM_SETAUTOCORRECTPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455771"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="d6b81-104">\_Mensagem em SETAUTOCORRECTPROC</span><span class="sxs-lookup"><span data-stu-id="d6b81-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="d6b81-105">Define o procedimento de retorno de chamada da AutoCorreção atual.</span><span class="sxs-lookup"><span data-stu-id="d6b81-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="d6b81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6b81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6b81-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6b81-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b81-108">A função de retorno de chamada [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="d6b81-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d6b81-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6b81-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6b81-110">Não usado; deve ser zero</span><span class="sxs-lookup"><span data-stu-id="d6b81-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6b81-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6b81-111">Return value</span></span>

<span data-ttu-id="d6b81-112">Se a operação for concluída com sucesso, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="d6b81-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="d6b81-113">Se a operação falhar, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d6b81-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b81-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6b81-114">Requirements</span></span>



| <span data-ttu-id="d6b81-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6b81-115">Requirement</span></span> | <span data-ttu-id="d6b81-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d6b81-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b81-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6b81-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d6b81-118">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d6b81-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d6b81-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6b81-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d6b81-120">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d6b81-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6b81-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6b81-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6b81-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6b81-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b81-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b81-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b81-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="d6b81-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="d6b81-125">**em \_ CALLAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="d6b81-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="d6b81-126">**em \_ GETAUTOCORRECTPROC**</span><span class="sxs-lookup"><span data-stu-id="d6b81-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





