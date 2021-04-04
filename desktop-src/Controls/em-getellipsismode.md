---
title: Mensagem de EM_GETELLIPSISMODE (RichEdit. h)
description: Recupera o modo de reticências atual.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Controles de EM_GETELLIPSISMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085591"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="ddd99-104">\_Mensagem em getreticências</span><span class="sxs-lookup"><span data-stu-id="ddd99-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="ddd99-105">Recupera o modo de reticências atual.</span><span class="sxs-lookup"><span data-stu-id="ddd99-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="ddd99-106">Quando habilitado, uma reticências () é exibida para texto que não se encaixa na janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="ddd99-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="ddd99-107">As reticências só são usadas quando o controle não está ativo.</span><span class="sxs-lookup"><span data-stu-id="ddd99-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="ddd99-108">Quando ativas, as barras de rolagem são usadas para revelar texto que não se encaixa na janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="ddd99-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="ddd99-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddd99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddd99-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddd99-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd99-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ddd99-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ddd99-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddd99-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddd99-113">Ponteiro para um DWORD que recebe um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddd99-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="ddd99-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ddd99-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="ddd99-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ddd99-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="ddd99-116"><dt>**RETICÊNCIAs \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd99-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="ddd99-117">Nenhuma elipse é usada.</span><span class="sxs-lookup"><span data-stu-id="ddd99-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="ddd99-118"><dt>**fim da elipse \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd99-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="ddd99-119">Reticências no final (quebra forçada).</span><span class="sxs-lookup"><span data-stu-id="ddd99-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="ddd99-120"><dt>**palavra de RETICÊNCIAs \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddd99-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="ddd99-121">Reticências no final (quebra de palavra).</span><span class="sxs-lookup"><span data-stu-id="ddd99-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddd99-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddd99-122">Return value</span></span>

<span data-ttu-id="ddd99-123">Se wParam for 0 e lParam não for NULL, o valor de retorno será igual a TRUE; caso contrário, o valor de retorno será igual a falso.</span><span class="sxs-lookup"><span data-stu-id="ddd99-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd99-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddd99-124">Requirements</span></span>



| <span data-ttu-id="ddd99-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddd99-125">Requirement</span></span> | <span data-ttu-id="ddd99-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ddd99-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd99-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddd99-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd99-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ddd99-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ddd99-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddd99-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd99-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ddd99-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddd99-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddd99-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd99-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd99-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd99-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddd99-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd99-134">**em \_ setreticências**</span><span class="sxs-lookup"><span data-stu-id="ddd99-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="ddd99-135">**em \_ getreticências**</span><span class="sxs-lookup"><span data-stu-id="ddd99-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





