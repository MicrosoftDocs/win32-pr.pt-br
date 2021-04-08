---
title: Mensagem de TB_GETBUTTONINFO (commctrl. h)
description: Recupera informações estendidas para um botão em uma barra de ferramentas.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Controles de TB_GETBUTTONINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086529"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="c84e3-104">TB de \_ mensagem GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="c84e3-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="c84e3-105">Recupera informações estendidas para um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="c84e3-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c84e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c84e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84e3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c84e3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c84e3-108">Identificador de comando do botão.</span><span class="sxs-lookup"><span data-stu-id="c84e3-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="c84e3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c84e3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c84e3-110">Ponteiro para uma estrutura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que recebe as informações do botão.</span><span class="sxs-lookup"><span data-stu-id="c84e3-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="c84e3-111">Os membros **cbSize** e **dwMask** desta estrutura devem ser preenchidos antes do envio desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="c84e3-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84e3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c84e3-112">Return value</span></span>

<span data-ttu-id="c84e3-113">Retorna o índice de base zero do botão ou-1 se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="c84e3-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84e3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c84e3-114">Remarks</span></span>

<span data-ttu-id="c84e3-115">Quando você usa caracteres de [**\_ INSERTBUTTON**](tb-insertbutton.md) de [**TB \_**](tb-addbuttons.md) ou TB para posicionar os botões na barra de ferramentas, o texto do botão é normalmente especificado por seu índice de pool de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c84e3-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="c84e3-116">**TB \_ GETBUTTONINFO** não recuperará essa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c84e3-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="c84e3-117">Para usar **TB \_ GETBUTTONINFO** para recuperar o texto do botão, você deve primeiro definir a cadeia de texto com [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md).</span><span class="sxs-lookup"><span data-stu-id="c84e3-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="c84e3-118">Depois de definir o texto do botão com **TB \_ SETBUTTONINFO**, você não poderá mais usar o índice do pool de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c84e3-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84e3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84e3-119">Requirements</span></span>



| <span data-ttu-id="c84e3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84e3-120">Requirement</span></span> | <span data-ttu-id="c84e3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c84e3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c84e3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c84e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c84e3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c84e3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c84e3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c84e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c84e3-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c84e3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c84e3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c84e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84e3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c84e3-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c84e3-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c84e3-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c84e3-129">**TB \_ GETBUTTONINFOW** (Unicode) e **TB \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c84e3-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c84e3-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c84e3-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c84e3-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c84e3-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c84e3-132">**TB de \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="c84e3-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="c84e3-133">**TB de \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="c84e3-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





