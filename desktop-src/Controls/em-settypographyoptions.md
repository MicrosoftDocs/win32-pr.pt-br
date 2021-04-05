---
title: Mensagem de EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Define o estado atual das opções de tipografia de um controle de edição rico.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Controles de EM_SETTYPOGRAPHYOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918614"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="1f0ac-104">\_Mensagem em SETtipografiaoptions</span><span class="sxs-lookup"><span data-stu-id="1f0ac-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="1f0ac-105">Define o estado atual das opções de tipografia de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f0ac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0ac-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f0ac-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f0ac-108">Especifica um ou ambos os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="1f0ac-109">Valor</span><span class="sxs-lookup"><span data-stu-id="1f0ac-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="1f0ac-110">Significado</span><span class="sxs-lookup"><span data-stu-id="1f0ac-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="1f0ac-111"><dt>**Para \_ ADVANCEDTYPOGRAPHY**</dt></span><span class="sxs-lookup"><span data-stu-id="1f0ac-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="1f0ac-112">A quebra de linha avançada e a formatação de linha estão ativadas.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="1f0ac-113"><dt>**PARA \_ SIMPLELINEBREAK**</dt></span><span class="sxs-lookup"><span data-stu-id="1f0ac-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="1f0ac-114">Quebra de linha mais rápida para texto simples (requer **\_ ADVANCEDTYPOGRAPHY**).</span><span class="sxs-lookup"><span data-stu-id="1f0ac-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="1f0ac-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f0ac-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f0ac-116">Uma máscara que consiste em um ou mais dos sinalizadores em *wParam*.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="1f0ac-117">Somente os sinalizadores definidos nesta máscara serão definidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="1f0ac-118">Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0ac-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f0ac-119">Return value</span></span>

<span data-ttu-id="1f0ac-120">Retornará **true** se *wParam* for válido, caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0ac-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f0ac-121">Remarks</span></span>

<span data-ttu-id="1f0ac-122">A quebra de linha avançada é ativada automaticamente pelo controle de edição rico quando necessário, como para lidar com scripts complexos, como árabe e Hebraico, e para matemática.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="1f0ac-123">Eles também são necessários para parágrafos justificados, hifenização e outros recursos tipográficos.</span><span class="sxs-lookup"><span data-stu-id="1f0ac-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0ac-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f0ac-124">Requirements</span></span>



| <span data-ttu-id="1f0ac-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f0ac-125">Requirement</span></span> | <span data-ttu-id="1f0ac-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1f0ac-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0ac-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f0ac-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1f0ac-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f0ac-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f0ac-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f0ac-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1f0ac-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f0ac-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f0ac-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1f0ac-131">Redistributable</span></span><br/>          | <span data-ttu-id="1f0ac-132">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="1f0ac-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="1f0ac-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f0ac-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f0ac-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f0ac-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f0ac-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f0ac-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f0ac-136">**em \_ GETtypographyoptions**</span><span class="sxs-lookup"><span data-stu-id="1f0ac-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





