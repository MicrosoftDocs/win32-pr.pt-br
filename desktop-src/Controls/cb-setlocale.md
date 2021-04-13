---
title: Mensagem de CB_SETLOCALE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETlocalização de CB para definir a localidade atual da caixa de combinação. Se a caixa de combinação tiver o \_ estilo de classificação CBS e as cadeias de caracteres forem adicionadas usando CB \_ AddString, a localidade de uma caixa de combinação afetará a forma como os itens de lista são classificados.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- Controles de CB_SETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025f33dc8ba236965a98ca984446b04846ecd2ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455457"
---
# <a name="cb_setlocale-message"></a><span data-ttu-id="653ba-105">\_Mensagem SETlocal do CB</span><span class="sxs-lookup"><span data-stu-id="653ba-105">CB\_SETLOCALE message</span></span>

<span data-ttu-id="653ba-106">Um aplicativo envia uma mensagem de **\_ setlocalização de CB** para definir a localidade atual da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="653ba-106">An application sends a **CB\_SETLOCALE** message to set the current locale of the combo box.</span></span> <span data-ttu-id="653ba-107">Se a caixa de combinação tiver o estilo de [**\_ classificação CBS**](combo-box-styles.md) e as cadeias de caracteres forem adicionadas usando [**CB \_ AddString**](cb-addstring.md), a localidade de uma caixa de combinação afetará a forma como os itens de lista são classificados.</span><span class="sxs-lookup"><span data-stu-id="653ba-107">If the combo box has the [**CBS\_SORT**](combo-box-styles.md) style and strings are added using [**CB\_ADDSTRING**](cb-addstring.md), the locale of a combo box affects how list items are sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="653ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="653ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="653ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="653ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="653ba-110">Especifica o identificador de localidade para a caixa de combinação a ser usada para classificação ao adicionar texto.</span><span class="sxs-lookup"><span data-stu-id="653ba-110">Specifies the locale identifier for the combo box to use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="653ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="653ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="653ba-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="653ba-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="653ba-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="653ba-113">Return value</span></span>

<span data-ttu-id="653ba-114">O valor de retorno é o identificador de localidade anterior.</span><span class="sxs-lookup"><span data-stu-id="653ba-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="653ba-115">Se *wParam* especificar uma localidade não instalada no sistema, o valor de retorno será CB \_ Err e a localidade da caixa de combinação atual não será alterada.</span><span class="sxs-lookup"><span data-stu-id="653ba-115">If *wParam* specifies a locale not installed on the system, the return value is CB\_ERR and the current combo box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="653ba-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="653ba-116">Remarks</span></span>

<span data-ttu-id="653ba-117">Use a macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir um identificador de localidade e a macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) para construir um identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="653ba-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier and the [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) macro to construct a language identifier.</span></span> <span data-ttu-id="653ba-118">O identificador de idioma é composto por um identificador de idioma primário e um identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="653ba-118">The language identifier is made up of a primary language identifier and a sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="653ba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653ba-119">Requirements</span></span>



| <span data-ttu-id="653ba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="653ba-120">Requirement</span></span> | <span data-ttu-id="653ba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="653ba-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653ba-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="653ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="653ba-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="653ba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="653ba-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="653ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="653ba-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="653ba-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="653ba-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="653ba-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="653ba-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="653ba-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653ba-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="653ba-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="653ba-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="653ba-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="653ba-130">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="653ba-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="653ba-131">**\_ISlocalização CB**</span><span class="sxs-lookup"><span data-stu-id="653ba-131">**CB\_GETLOCALE**</span></span>](cb-getlocale.md)
</dt> <dt>

<span data-ttu-id="653ba-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="653ba-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="653ba-133">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="653ba-133">**MAKELANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[<span data-ttu-id="653ba-134">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="653ba-134">**MAKELCID**</span></span>](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

