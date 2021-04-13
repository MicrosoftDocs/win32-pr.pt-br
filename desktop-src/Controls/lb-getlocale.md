---
title: Mensagem de LB_GETLOCALE (WinUser. h)
description: Obtém a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o \_ estilo de classificação lbs) e o texto adicionado pela mensagem do lb \_ AddString.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Controles de LB_GETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455337"
---
# <a name="lb_getlocale-message"></a><span data-ttu-id="91b55-105">\_Mensagem de GETlocalize do lb</span><span class="sxs-lookup"><span data-stu-id="91b55-105">LB\_GETLOCALE message</span></span>

<span data-ttu-id="91b55-106">Obtém a localidade atual da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="91b55-106">Gets the current locale of the list box.</span></span> <span data-ttu-id="91b55-107">Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo de [**\_ classificação lbs**](list-box-styles.md) ) e o texto adicionado pela mensagem do [**lb \_ AddString**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="91b55-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="91b55-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91b55-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b55-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91b55-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91b55-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="91b55-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="91b55-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91b55-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91b55-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="91b55-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b55-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91b55-113">Return value</span></span>

<span data-ttu-id="91b55-114">O valor de retorno especifica a localidade atual da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="91b55-114">The return value specifies the current locale of the list box.</span></span> <span data-ttu-id="91b55-115">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o código de país/região e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="91b55-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="91b55-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="91b55-116">Remarks</span></span>

<span data-ttu-id="91b55-117">O identificador de idioma consiste em um identificador de subidioma e um identificador de idioma primário.</span><span class="sxs-lookup"><span data-stu-id="91b55-117">The language identifier consists of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="91b55-118">Use a macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) para extrair o identificador de idioma primário do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) do valor de retorno e a macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) para extrair o identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="91b55-118">Use the [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro to extract the primary language identifier from the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro to extract the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b55-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91b55-119">Requirements</span></span>



| <span data-ttu-id="91b55-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="91b55-120">Requirement</span></span> | <span data-ttu-id="91b55-121">Valor</span><span class="sxs-lookup"><span data-stu-id="91b55-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b55-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91b55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="91b55-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91b55-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="91b55-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91b55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="91b55-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91b55-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91b55-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91b55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="91b55-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91b55-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b55-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="91b55-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="91b55-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="91b55-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="91b55-130">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="91b55-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="91b55-131">**LB \_ SETlocale**</span><span class="sxs-lookup"><span data-stu-id="91b55-131">**LB\_SETLOCALE**</span></span>](lb-setlocale.md)
</dt> <dt>

<span data-ttu-id="91b55-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="91b55-132">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="91b55-133">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="91b55-133">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="91b55-134">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="91b55-134">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

