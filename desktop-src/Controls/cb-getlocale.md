---
title: Mensagem de CB_GETLOCALE (WinUser. h)
description: Obtém a localidade atual da caixa de combinação. A localidade é usada para determinar a ordem de classificação correta do texto exibido para caixas de combinação com o \_ estilo de classificação CBS e o texto adicionado usando a \_ mensagem createstring CB.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Controles de CB_GETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009359"
---
# <a name="cb_getlocale-message"></a><span data-ttu-id="52f12-105">\_Mensagem de GETlocalização CB</span><span class="sxs-lookup"><span data-stu-id="52f12-105">CB\_GETLOCALE message</span></span>

<span data-ttu-id="52f12-106">Obtém a localidade atual da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="52f12-106">Gets the current locale of the combo box.</span></span> <span data-ttu-id="52f12-107">A localidade é usada para determinar a ordem de classificação correta do texto exibido para caixas de combinação com o estilo de [**\_ classificação CBS**](combo-box-styles.md) e o texto adicionado usando a mensagem [**\_ createstring CB**](cb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="52f12-107">The locale is used to determine the correct sorting order of displayed text for combo boxes with the [**CBS\_SORT**](combo-box-styles.md) style and text added by using the [**CB\_ADDSTRING**](cb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="52f12-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52f12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f12-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52f12-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52f12-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="52f12-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="52f12-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52f12-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52f12-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="52f12-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f12-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52f12-113">Return value</span></span>

<span data-ttu-id="52f12-114">O valor de retorno especifica a localidade atual da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="52f12-114">The return value specifies the current locale of the combo box.</span></span> <span data-ttu-id="52f12-115">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém o código de país/região e o [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="52f12-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the country/region code and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the language identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f12-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="52f12-116">Remarks</span></span>

<span data-ttu-id="52f12-117">O identificador de idioma é composto por um identificador de subidioma e um identificador de idioma primário.</span><span class="sxs-lookup"><span data-stu-id="52f12-117">The language identifier is made up of a sublanguage identifier and a primary language identifier.</span></span> <span data-ttu-id="52f12-118">A macro [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) Obtém o identificador de idioma primário e a macro [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) Obtém o identificador do subidioma.</span><span class="sxs-lookup"><span data-stu-id="52f12-118">The [**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid) macro obtains the primary language identifier and the [**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid) macro obtains the sublanguage identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f12-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f12-119">Requirements</span></span>



| <span data-ttu-id="52f12-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f12-120">Requirement</span></span> | <span data-ttu-id="52f12-121">Valor</span><span class="sxs-lookup"><span data-stu-id="52f12-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f12-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f12-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52f12-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52f12-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52f12-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52f12-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52f12-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52f12-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="52f12-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52f12-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f12-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="52f12-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f12-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f12-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="52f12-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="52f12-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="52f12-130">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="52f12-130">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="52f12-131">**setlocalar do CB \_**</span><span class="sxs-lookup"><span data-stu-id="52f12-131">**CB\_SETLOCALE**</span></span>](cb-setlocale.md)
</dt> <dt>

<span data-ttu-id="52f12-132">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="52f12-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="52f12-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52f12-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="52f12-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="52f12-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="52f12-135">**PRIMARYLANGID**</span><span class="sxs-lookup"><span data-stu-id="52f12-135">**PRIMARYLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[<span data-ttu-id="52f12-136">**SUBLANGID**</span><span class="sxs-lookup"><span data-stu-id="52f12-136">**SUBLANGID**</span></span>](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

