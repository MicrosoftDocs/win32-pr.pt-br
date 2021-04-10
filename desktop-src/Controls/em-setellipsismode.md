---
title: Mensagem de EM_SETELLIPSISMODE (RichEdit. h)
description: Essa mensagem define o modo de reticências atual.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- Controles de EM_SETELLIPSISMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009658"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="8bf20-104">\_Mensagem em setreticências</span><span class="sxs-lookup"><span data-stu-id="8bf20-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="8bf20-105">Essa mensagem define o modo de reticências atual.</span><span class="sxs-lookup"><span data-stu-id="8bf20-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="8bf20-106">Quando habilitado, uma reticências () é exibida para texto que não se encaixa na janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="8bf20-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="8bf20-107">As reticências só são usadas quando o controle não está ativo.</span><span class="sxs-lookup"><span data-stu-id="8bf20-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="8bf20-108">Quando ativas, as barras de rolagem são usadas para revelar texto que não se encaixa na janela de exibição.</span><span class="sxs-lookup"><span data-stu-id="8bf20-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="8bf20-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bf20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf20-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bf20-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf20-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8bf20-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8bf20-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bf20-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bf20-113">Um DWORD que recebe um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8bf20-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="8bf20-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf20-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="8bf20-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8bf20-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="8bf20-116"><dt>**RETICÊNCIAs \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf20-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="8bf20-117">Nenhuma elipse é usada.</span><span class="sxs-lookup"><span data-stu-id="8bf20-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="8bf20-118"><dt>**fim da elipse \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf20-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="8bf20-119">Reticências no final (quebra forçada).</span><span class="sxs-lookup"><span data-stu-id="8bf20-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="8bf20-120"><dt>**palavra de RETICÊNCIAs \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf20-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="8bf20-121">Reticências no final (quebra de palavra).</span><span class="sxs-lookup"><span data-stu-id="8bf20-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="8bf20-122">Todos os bits para esses valores se encaixam na **\_ máscara de reticências**.</span><span class="sxs-lookup"><span data-stu-id="8bf20-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf20-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8bf20-123">Return value</span></span>

<span data-ttu-id="8bf20-124">Se wParam for 0 e lParam for um dos valores na tabela acima, o valor de retorno será igual a TRUE; caso contrário, o valor de retorno será igual a falso.</span><span class="sxs-lookup"><span data-stu-id="8bf20-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf20-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf20-125">Requirements</span></span>



| <span data-ttu-id="8bf20-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf20-126">Requirement</span></span> | <span data-ttu-id="8bf20-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf20-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf20-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf20-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf20-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bf20-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8bf20-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf20-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf20-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bf20-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bf20-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8bf20-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf20-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf20-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf20-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bf20-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf20-135">**em \_ GETreticênciamode**</span><span class="sxs-lookup"><span data-stu-id="8bf20-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="8bf20-136">**em \_ getreticências**</span><span class="sxs-lookup"><span data-stu-id="8bf20-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





