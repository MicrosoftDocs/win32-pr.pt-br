---
title: Mensagem de EM_GETELLIPSISSTATE (RichEdit. h)
description: Recupera o estado de reticências atual.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- Controles de EM_GETELLIPSISSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455185"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="96749-104">\_Mensagem em getreticências</span><span class="sxs-lookup"><span data-stu-id="96749-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="96749-105">Recupera o estado de reticências atual.</span><span class="sxs-lookup"><span data-stu-id="96749-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="96749-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96749-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96749-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96749-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96749-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="96749-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="96749-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96749-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96749-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="96749-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96749-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96749-111">Return value</span></span>

<span data-ttu-id="96749-112">O valor de retorno será TRUE se uma elipse estiver sendo exibida e FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="96749-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96749-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96749-113">Requirements</span></span>



| <span data-ttu-id="96749-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="96749-114">Requirement</span></span> | <span data-ttu-id="96749-115">Valor</span><span class="sxs-lookup"><span data-stu-id="96749-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96749-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96749-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96749-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="96749-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="96749-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96749-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96749-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="96749-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96749-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96749-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96749-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="96749-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96749-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="96749-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96749-123">**em \_ GETreticênciamode**</span><span class="sxs-lookup"><span data-stu-id="96749-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="96749-124">**em \_ setreticências**</span><span class="sxs-lookup"><span data-stu-id="96749-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





