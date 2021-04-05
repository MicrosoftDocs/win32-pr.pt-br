---
title: Mensagem de EM_SETLANGOPTIONS (RichEdit. h)
description: Define opções para o IME (editor de método de entrada) e suporte a idiomas asiáticos em um controle de edição rico.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Controles de EM_SETLANGOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918347"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="a8799-104">\_Mensagem em SETlangoptions</span><span class="sxs-lookup"><span data-stu-id="a8799-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="a8799-105">Define opções para o IME (editor de método de entrada) e suporte a idiomas asiáticos em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="a8799-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8799-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8799-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8799-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8799-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a8799-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a8799-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8799-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8799-110">Especifica as opções de idioma.</span><span class="sxs-lookup"><span data-stu-id="a8799-110">Specifies the language options.</span></span> <span data-ttu-id="a8799-111">Para obter uma lista de valores possíveis, consulte em [**\_ getlangoptions**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="a8799-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8799-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8799-112">Return value</span></span>

<span data-ttu-id="a8799-113">Essa mensagem retorna um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="a8799-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8799-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8799-114">Remarks</span></span>

<span data-ttu-id="a8799-115">A mensagem em **\_ setlangoptions** controla o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8799-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="a8799-116">Associação de fonte automática.</span><span class="sxs-lookup"><span data-stu-id="a8799-116">Automatic font binding.</span></span>
-   <span data-ttu-id="a8799-117">Alternância automática de teclado.</span><span class="sxs-lookup"><span data-stu-id="a8799-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="a8799-118">Ajuste de tamanho de fonte automático.</span><span class="sxs-lookup"><span data-stu-id="a8799-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="a8799-119">Uso de fontes padrão de interface do usuário em vez de fontes padrão de documento.</span><span class="sxs-lookup"><span data-stu-id="a8799-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="a8799-120">Notificações ao cliente durante a composição do IME.</span><span class="sxs-lookup"><span data-stu-id="a8799-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="a8799-121">Como o IME anula o modo de composição.</span><span class="sxs-lookup"><span data-stu-id="a8799-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="a8799-122">Verificação ortográfica, AutoCorreção e previsão de teclado de toque.</span><span class="sxs-lookup"><span data-stu-id="a8799-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="a8799-123">Essa mensagem define os valores de todos os sinalizadores de opção de idioma.</span><span class="sxs-lookup"><span data-stu-id="a8799-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="a8799-124">Para alterar um subconjunto dos sinalizadores, envie a mensagem em [**\_ getlangoptions**](em-getlangoptions.md) para obter os sinalizadores de opção atuais, altere os sinalizadores que você precisa alterar e, em seguida, envie a mensagem em **\_ setlangoptions** com o resultado.</span><span class="sxs-lookup"><span data-stu-id="a8799-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8799-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8799-125">Requirements</span></span>



| <span data-ttu-id="a8799-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8799-126">Requirement</span></span> | <span data-ttu-id="a8799-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a8799-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8799-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8799-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8799-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8799-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8799-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8799-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8799-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8799-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8799-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8799-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8799-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8799-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8799-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8799-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8799-135">**em \_ GETlangoptions**</span><span class="sxs-lookup"><span data-stu-id="a8799-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





