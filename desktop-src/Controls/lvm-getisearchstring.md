---
title: Mensagem de LVM_GETISEARCHSTRING (commctrl. h)
description: Recupera a cadeia de caracteres de pesquisa incremental de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetISearchString do ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Controles de LVM_GETISEARCHSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455749"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="c672a-105">\_Mensagem GETISEARCHSTRING LVM</span><span class="sxs-lookup"><span data-stu-id="c672a-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="c672a-106">Recupera a cadeia de caracteres de pesquisa incremental de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="c672a-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="c672a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetISearchString do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="c672a-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c672a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c672a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c672a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c672a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c672a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c672a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c672a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c672a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c672a-112">Ponteiro para um buffer que recebe a cadeia de caracteres de pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="c672a-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="c672a-113">Para recuperar apenas o comprimento da cadeia de caracteres, defina *lParam* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c672a-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c672a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c672a-114">Return value</span></span>

<span data-ttu-id="c672a-115">Retorna o número de caracteres na cadeia de caracteres de pesquisa incremental, não incluindo o caractere nulo de terminação ou zero se o controle de exibição de lista não estiver no modo de pesquisa incremental.</span><span class="sxs-lookup"><span data-stu-id="c672a-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="c672a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c672a-116">Remarks</span></span>

<span data-ttu-id="c672a-117">**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="c672a-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="c672a-118">Essa mensagem não fornece uma maneira de saber o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="c672a-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="c672a-119">Se você usar essa mensagem, primeiro chame a mensagem transmitindo **NULL** no *lParam*; isso retorna o número de caracteres, excluindo **NULL** que são necessários.</span><span class="sxs-lookup"><span data-stu-id="c672a-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="c672a-120">Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c672a-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="c672a-121">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="c672a-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="c672a-122">A seqüência de caracteres de *pesquisa incremental* é a sequência de caracteres que o usuário digita enquanto a exibição de lista tem o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="c672a-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="c672a-123">Cada vez que o usuário digita um caractere, o sistema anexa o caractere à cadeia de caracteres de pesquisa e, em seguida, procura um item correspondente.</span><span class="sxs-lookup"><span data-stu-id="c672a-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="c672a-124">Se o sistema encontrar uma correspondência, ele selecionará o item e, se necessário, o rolará para o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="c672a-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="c672a-125">Um período de tempo limite é associado a cada caractere que o usuário digita.</span><span class="sxs-lookup"><span data-stu-id="c672a-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="c672a-126">Se o período de tempo limite expirar antes de o usuário digitar outro caractere, a cadeia de caracteres de pesquisa incremental será redefinida.</span><span class="sxs-lookup"><span data-stu-id="c672a-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="c672a-127">Verifique se o buffer é grande o suficiente para manter a cadeia de caracteres e o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c672a-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="c672a-128">Se for muito pequeno, será resultado uma falha de página inválida imediata.</span><span class="sxs-lookup"><span data-stu-id="c672a-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="c672a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c672a-129">Requirements</span></span>



| <span data-ttu-id="c672a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c672a-130">Requirement</span></span> | <span data-ttu-id="c672a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c672a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c672a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c672a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c672a-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c672a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c672a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c672a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c672a-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c672a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c672a-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c672a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c672a-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c672a-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c672a-138">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c672a-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c672a-139">**LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c672a-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





