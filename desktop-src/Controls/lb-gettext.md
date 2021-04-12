---
title: Mensagem de LB_GETTEXT (WinUser. h)
description: Obtém uma cadeia de caracteres de uma caixa de listagem.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Controles de LB_GETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455660"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="71de2-104">A \_ mensagem GETtext de lb</span><span class="sxs-lookup"><span data-stu-id="71de2-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="71de2-105">Obtém uma cadeia de caracteres de uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="71de2-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="71de2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71de2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71de2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71de2-108">O índice de base zero da cadeia de caracteres a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="71de2-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="71de2-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="71de2-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="71de2-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="71de2-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="71de2-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="71de2-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="71de2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71de2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71de2-113">Um ponteiro para o buffer que receberá a cadeia de caracteres; é o tipo **LPTSTR** , que é posteriormente convertido em um **lParam**.</span><span class="sxs-lookup"><span data-stu-id="71de2-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="71de2-114">O buffer deve ter espaço suficiente para a cadeia de caracteres e um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="71de2-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="71de2-115">Uma mensagem de [**\_ GETTEXTLEN de lb**](lb-gettextlen.md) pode ser enviada antes da mensagem de **\_ gettext do lb** para recuperar o comprimento, em **TCHAR** s, da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="71de2-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71de2-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71de2-116">Return value</span></span>

<span data-ttu-id="71de2-117">O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="71de2-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="71de2-118">Se *wParam* não especificar um índice válido, o valor de retorno será um \_ erro de lb.</span><span class="sxs-lookup"><span data-stu-id="71de2-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="71de2-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="71de2-119">Remarks</span></span>

<span data-ttu-id="71de2-120">Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o buffer apontado pelo parâmetro *lParam* receberá o valor associado ao item (os dados do item).</span><span class="sxs-lookup"><span data-stu-id="71de2-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="71de2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71de2-121">Requirements</span></span>



| <span data-ttu-id="71de2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71de2-122">Requirement</span></span> | <span data-ttu-id="71de2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="71de2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71de2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71de2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71de2-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71de2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="71de2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71de2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71de2-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71de2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="71de2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71de2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71de2-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71de2-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71de2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="71de2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71de2-131">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="71de2-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





