---
title: Mensagem de EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Retorna o estado atual das opções de tipografia de um controle de edição rico.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Controles de EM_GETTYPOGRAPHYOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086031"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="54a0c-104">\_Mensagem em GETtipografiaoptions</span><span class="sxs-lookup"><span data-stu-id="54a0c-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="54a0c-105">Retorna o estado atual das opções de tipografia de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="54a0c-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="54a0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54a0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54a0c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54a0c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a0c-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="54a0c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="54a0c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54a0c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54a0c-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="54a0c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54a0c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54a0c-111">Return value</span></span>

<span data-ttu-id="54a0c-112">Retorna as opções de tipografia atuais.</span><span class="sxs-lookup"><span data-stu-id="54a0c-112">Returns the current typography options.</span></span> <span data-ttu-id="54a0c-113">Para obter uma lista de opções, consulte em [**\_ settypographyoptions**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="54a0c-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54a0c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="54a0c-114">Remarks</span></span>

<span data-ttu-id="54a0c-115">Você pode ativar a quebra de linha avançada enviando a mensagem em [**\_ settipografiaoptions**](em-settypographyoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="54a0c-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="54a0c-116">A quebra de linha avançada e normal também pode ser ativada automaticamente pelo controle de edição avançada se for necessário para determinados idiomas.</span><span class="sxs-lookup"><span data-stu-id="54a0c-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="54a0c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54a0c-117">Requirements</span></span>



| <span data-ttu-id="54a0c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54a0c-118">Requirement</span></span> | <span data-ttu-id="54a0c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="54a0c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54a0c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54a0c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54a0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54a0c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54a0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54a0c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="54a0c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54a0c-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="54a0c-124">Redistributable</span></span><br/>          | <span data-ttu-id="54a0c-125">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="54a0c-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="54a0c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54a0c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a0c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="54a0c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54a0c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="54a0c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="54a0c-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="54a0c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54a0c-130">**em \_ SETtipografiaoptions**</span><span class="sxs-lookup"><span data-stu-id="54a0c-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="54a0c-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="54a0c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54a0c-132">Sobre os controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="54a0c-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





