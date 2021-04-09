---
title: Mensagem de TB_GETSTRING (commctrl. h)
description: Recupera uma cadeia de caracteres do pool de cadeias de caracteres de uma barra de ferramentas.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Controles de TB_GETSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009125"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="d36e0-104">\_Cadeia de caracteres GETstring de TB</span><span class="sxs-lookup"><span data-stu-id="d36e0-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="d36e0-105">Recupera uma cadeia de caracteres do pool de cadeias de caracteres de uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d36e0-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="d36e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d36e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d36e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d36e0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d36e0-108">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o comprimento do buffer de *lParam* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="d36e0-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="d36e0-109">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d36e0-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="d36e0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d36e0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d36e0-111">Ponteiro para um buffer usado para retornar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d36e0-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d36e0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d36e0-112">Return value</span></span>

<span data-ttu-id="d36e0-113">Retorna o comprimento da cadeia de caracteres se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d36e0-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d36e0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d36e0-114">Remarks</span></span>

<span data-ttu-id="d36e0-115">Essa mensagem retorna a cadeia de caracteres especificada do pool de cadeias de caracteres da barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="d36e0-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="d36e0-116">Ele não corresponde necessariamente à cadeia de texto que está sendo exibida atualmente por um botão.</span><span class="sxs-lookup"><span data-stu-id="d36e0-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="d36e0-117">Para recuperar a cadeia de texto atual de um botão, envie a barra de ferramentas uma mensagem de [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md) .</span><span class="sxs-lookup"><span data-stu-id="d36e0-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d36e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d36e0-118">Requirements</span></span>



| <span data-ttu-id="d36e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d36e0-119">Requirement</span></span> | <span data-ttu-id="d36e0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d36e0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d36e0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d36e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d36e0-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d36e0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d36e0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d36e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d36e0-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d36e0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d36e0-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d36e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d36e0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d36e0-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d36e0-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d36e0-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d36e0-128">**TB \_ GETSTRINGW** (Unicode) e **TB \_ getstringa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d36e0-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d36e0-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d36e0-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="d36e0-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d36e0-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d36e0-131">**\_caracteres ADDstring de TB**</span><span class="sxs-lookup"><span data-stu-id="d36e0-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="d36e0-132">**hiperbotãos de TB \_**</span><span class="sxs-lookup"><span data-stu-id="d36e0-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="d36e0-133">**TB de \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="d36e0-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

