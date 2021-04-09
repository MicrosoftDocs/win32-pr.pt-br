---
title: Mensagem de TB_GETBUTTONTEXT (commctrl. h)
description: Recupera o texto de exibição de um botão em uma barra de ferramentas.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Controles de TB_GETBUTTONTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085723"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="2ddce-104">TB de \_ mensagem GETBUTTONTEXT</span><span class="sxs-lookup"><span data-stu-id="2ddce-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="2ddce-105">Recupera o texto de exibição de um botão em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="2ddce-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ddce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ddce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ddce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddce-108">Identificador de comando do botão cujo texto deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="2ddce-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="2ddce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ddce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ddce-110">Ponteiro para um buffer que recebe o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="2ddce-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddce-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ddce-111">Return value</span></span>

<span data-ttu-id="2ddce-112">Retorna o comprimento, em caracteres, da cadeia de caracteres apontada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2ddce-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="2ddce-113">O comprimento não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="2ddce-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="2ddce-114">Se não for bem-sucedida, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="2ddce-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ddce-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddce-115">Remarks</span></span>

<span data-ttu-id="2ddce-116">**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="2ddce-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="2ddce-117">Essa mensagem não fornece uma maneira de saber o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="2ddce-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="2ddce-118">Se você usar essa mensagem, primeiro chame a mensagem transmitindo **NULL** no *lParam*; isso retorna o número de caracteres, excluindo **NULL** que são necessários.</span><span class="sxs-lookup"><span data-stu-id="2ddce-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="2ddce-119">Em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2ddce-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="2ddce-120">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="2ddce-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="2ddce-121">A cadeia de caracteres retornada corresponde ao texto que é exibido no momento pelo botão.</span><span class="sxs-lookup"><span data-stu-id="2ddce-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ddce-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddce-122">Requirements</span></span>



| <span data-ttu-id="2ddce-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddce-123">Requirement</span></span> | <span data-ttu-id="2ddce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2ddce-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddce-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddce-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ddce-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ddce-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ddce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddce-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ddce-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ddce-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ddce-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddce-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddce-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2ddce-131">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="2ddce-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2ddce-132">**TB \_ GETBUTTONTEXTW** (Unicode) e **TB \_ GETBUTTONTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2ddce-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="2ddce-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ddce-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ddce-134">**Referência**</span><span class="sxs-lookup"><span data-stu-id="2ddce-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ddce-135">**TB de \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="2ddce-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="2ddce-136">**TB \_ GETstring**</span><span class="sxs-lookup"><span data-stu-id="2ddce-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="2ddce-137">**TB de \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="2ddce-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





