---
title: Mensagem de TB_SETBUTTONINFO (commctrl. h)
description: Define as informações de um botão existente em uma barra de ferramentas.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Controles de TB_SETBUTTONINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824753"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="d2767-104">TB de \_ mensagem SETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="d2767-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="d2767-105">Define as informações de um botão existente em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d2767-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2767-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2767-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2767-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2767-108">Identificador de botão.</span><span class="sxs-lookup"><span data-stu-id="d2767-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d2767-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2767-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2767-110">Ponteiro para uma estrutura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) que contém as informações do novo botão.</span><span class="sxs-lookup"><span data-stu-id="d2767-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="d2767-111">Os membros **cbSize** e **dwMask** desta estrutura devem ser preenchidos antes do envio desta mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2767-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2767-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2767-112">Return value</span></span>

<span data-ttu-id="d2767-113">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="d2767-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2767-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2767-114">Remarks</span></span>

<span data-ttu-id="d2767-115">Normalmente, o texto é atribuído a botões quando eles são adicionados a uma barra de ferramentas especificando o índice de uma cadeia de caracteres no pool de cadeias da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d2767-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="d2767-116">Se você usar um **\_ SETBUTTONINFO TB** para atribuir um novo texto a um botão, ele substituirá permanentemente o texto do pool de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2767-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="d2767-117">Você pode alterar o texto chamando **TB \_ SETBUTTONINFO** novamente, mas não é possível reatribuir a cadeia de caracteres do pool de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2767-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2767-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2767-118">Requirements</span></span>



| <span data-ttu-id="d2767-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2767-119">Requirement</span></span> | <span data-ttu-id="d2767-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d2767-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2767-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2767-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d2767-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2767-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2767-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2767-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d2767-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2767-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2767-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2767-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2767-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2767-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d2767-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d2767-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d2767-128">**TB \_ SETBUTTONINFOW** (Unicode) e **TB \_ SETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d2767-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d2767-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2767-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2767-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d2767-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2767-131">**hiperbotãos de TB \_**</span><span class="sxs-lookup"><span data-stu-id="d2767-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="d2767-132">**TB de \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="d2767-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="d2767-133">**TB de \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d2767-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="d2767-134">**TB \_ GETstring**</span><span class="sxs-lookup"><span data-stu-id="d2767-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="d2767-135">**TB de \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d2767-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





