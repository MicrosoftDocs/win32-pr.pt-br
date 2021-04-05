---
title: Mensagem de CB_GETLBTEXT (WinUser. h)
description: Obtém uma cadeia de caracteres da lista de uma caixa de combinação.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Controles de CB_GETLBTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009361"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="6ea02-104">\_Mensagem de GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="6ea02-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="6ea02-105">Obtém uma cadeia de caracteres da lista de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6ea02-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ea02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ea02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ea02-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ea02-108">O índice de base zero da cadeia de caracteres a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="6ea02-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6ea02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ea02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ea02-110">Um ponteiro para o buffer que recebe a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ea02-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="6ea02-111">O buffer deve ter espaço suficiente para a cadeia de caracteres e um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="6ea02-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="6ea02-112">Você pode enviar uma mensagem [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) antes da mensagem **CB \_ GETLBTEXT** para recuperar o comprimento, em **TCHAR** s, da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ea02-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="6ea02-113">Se for uma cadeia de caracteres ANSI, esse será o número de bytes, mas se for uma cadeia de caracteres Unicode, esse será o número de personagens.</span><span class="sxs-lookup"><span data-stu-id="6ea02-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea02-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ea02-114">Return value</span></span>

<span data-ttu-id="6ea02-115">O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="6ea02-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="6ea02-116">Se *wParam* não especificar um índice válido, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6ea02-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ea02-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ea02-117">Remarks</span></span>

<span data-ttu-id="6ea02-118">**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="6ea02-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="6ea02-119">Essa mensagem não fornece uma maneira de saber o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="6ea02-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="6ea02-120">Se você usar essa mensagem, primeiro chame [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obter o número de caracteres necessários e, em seguida, chame a mensagem para recuperar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="6ea02-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="6ea02-121">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="6ea02-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="6ea02-122">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o buffer apontado por *lParam* receberá os dados associados ao item.</span><span class="sxs-lookup"><span data-stu-id="6ea02-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea02-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ea02-123">Requirements</span></span>



| <span data-ttu-id="6ea02-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ea02-124">Requirement</span></span> | <span data-ttu-id="6ea02-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6ea02-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea02-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ea02-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea02-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ea02-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6ea02-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ea02-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea02-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ea02-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6ea02-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ea02-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ea02-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ea02-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ea02-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ea02-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea02-133">**\_GETLBTEXTLEN CB**</span><span class="sxs-lookup"><span data-stu-id="6ea02-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





