---
title: Mensagem de EM_SETHANDLE (WinUser. h)
description: Define o identificador da memória que será usada por um controle de edição de várias linhas.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Controles de EM_SETHANDLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086187"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="24211-104">\_Mensagem em SEThandle</span><span class="sxs-lookup"><span data-stu-id="24211-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="24211-105">Define o identificador da memória que será usada por um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="24211-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="24211-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24211-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24211-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24211-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24211-108">Um identificador para o buffer de memória que o controle de edição usa para armazenar o texto atualmente exibido em vez de alocar sua própria memória.</span><span class="sxs-lookup"><span data-stu-id="24211-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="24211-109">Se necessário, o controle realoca essa memória.</span><span class="sxs-lookup"><span data-stu-id="24211-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="24211-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24211-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24211-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="24211-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24211-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24211-112">Return value</span></span>

<span data-ttu-id="24211-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="24211-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24211-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="24211-114">Remarks</span></span>

<span data-ttu-id="24211-115">Antes que um aplicativo defina um novo identificador de memória, ele deve enviar uma mensagem em em [**\_ GetHandle**](em-gethandle.md) para recuperar o identificador do buffer de memória atual e liberar essa memória.</span><span class="sxs-lookup"><span data-stu-id="24211-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="24211-116">Um controle de edição realoca automaticamente o buffer determinado sempre que ele precisa de espaço adicional para o texto, ou remove texto suficiente para que o espaço adicional não seja mais necessário.</span><span class="sxs-lookup"><span data-stu-id="24211-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="24211-117">O envio de uma mensagem em **\_ onhandle** limpa o buffer de desfazer (em [**\_ cancelamento**](em-canundo.md) retorna zero) e o sinalizador de modificação interna (em [**\_ GetModify**](em-getmodify.md) retorna zero).</span><span class="sxs-lookup"><span data-stu-id="24211-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="24211-118">A janela de controle de edição é redesenhada.</span><span class="sxs-lookup"><span data-stu-id="24211-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="24211-119">**Edição avançada:** Não há suporte para a mensagem em **\_ SetHandle** .</span><span class="sxs-lookup"><span data-stu-id="24211-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="24211-120">Os controles de edição avançados não armazenam texto como uma matriz simples de caracteres.</span><span class="sxs-lookup"><span data-stu-id="24211-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="24211-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24211-121">Requirements</span></span>



| <span data-ttu-id="24211-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="24211-122">Requirement</span></span> | <span data-ttu-id="24211-123">Valor</span><span class="sxs-lookup"><span data-stu-id="24211-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24211-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24211-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24211-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24211-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24211-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24211-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24211-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24211-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24211-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24211-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="24211-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24211-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24211-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="24211-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="24211-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="24211-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24211-132">**em \_ CANcelamento**</span><span class="sxs-lookup"><span data-stu-id="24211-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="24211-133">**em \_ GEThandle**</span><span class="sxs-lookup"><span data-stu-id="24211-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="24211-134">**em \_ GETmodify**</span><span class="sxs-lookup"><span data-stu-id="24211-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





