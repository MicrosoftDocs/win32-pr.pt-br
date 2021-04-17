---
title: Estilos de dica de ferramenta (CommCtrl. h)
description: Esta seção lista os estilos de controle usados com controles de dica de ferramenta.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752602"
---
# <a name="tooltip-styles"></a><span data-ttu-id="5744d-103">Estilos de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="5744d-103">Tooltip Styles</span></span>

<span data-ttu-id="5744d-104">Esta seção lista os estilos de controle usados com controles de dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5744d-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="5744d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="5744d-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="5744d-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="5744d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="5744d-107"><dt>**\_ALWAYSTIP TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="5744d-108">Indica que o controle ToolTip aparece quando o cursor está em uma ferramenta, mesmo que a janela do proprietário do controle ToolTip esteja inativa.</span><span class="sxs-lookup"><span data-stu-id="5744d-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="5744d-109">Sem esse estilo, a dica de ferramenta é exibida somente quando a janela do proprietário de ferramentas está ativa.</span><span class="sxs-lookup"><span data-stu-id="5744d-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="5744d-110"><dt>**balão de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="5744d-111">[Versão 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5744d-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="5744d-112">Indica que o controle ToolTip tem a aparência de um "balão" animado com cantos arredondados e uma haste apontando para o item.</span><span class="sxs-lookup"><span data-stu-id="5744d-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="5744d-113"><dt>**fechamento de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="5744d-114">Exibe um botão **fechar** na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5744d-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="5744d-115">Válido somente quando a dica de ferramenta tem o \_ estilo de balão TTS e um título; consulte [**\_ SetTitle TTM**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="5744d-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="5744d-116"><dt>**noanime de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="5744d-117">[Versão 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5744d-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="5744d-118">Desabilita a animação deslizante da dica de ferramenta nos sistemas Windows 98 e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5744d-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="5744d-119">Esse estilo é ignorado em sistemas anteriores.</span><span class="sxs-lookup"><span data-stu-id="5744d-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="5744d-120"><dt>**nofade de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="5744d-121">[Versão 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5744d-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="5744d-122">Desabilita a animação de dica de ferramenta de esmaecimento.</span><span class="sxs-lookup"><span data-stu-id="5744d-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="5744d-123"><dt>**NoPrefix de TTS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="5744d-124">Impede que o sistema retirasse caracteres de e comercial de uma cadeia de caracteres ou encerrando uma cadeia de caracteres em um caractere de tabulação.</span><span class="sxs-lookup"><span data-stu-id="5744d-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="5744d-125">Sem esse estilo, o sistema retira automaticamente os caracteres de e comercial e encerra uma cadeia de caracteres no primeiro caractere de tabulação.</span><span class="sxs-lookup"><span data-stu-id="5744d-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="5744d-126">Isso permite que um aplicativo use a mesma cadeia de caracteres como um item de menu e como texto em um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="5744d-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="5744d-127"><dt>**\_USEVISUALSTYLE TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="5744d-128">Usa hiperlinks com tema.</span><span class="sxs-lookup"><span data-stu-id="5744d-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="5744d-129">O tema definirá os estilos para todos os links na dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5744d-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="5744d-130">Esse estilo sempre exige que o TTF \_ PARSELINKS seja definido.</span><span class="sxs-lookup"><span data-stu-id="5744d-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="5744d-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5744d-131">Remarks</span></span>

<span data-ttu-id="5744d-132">Um controle ToolTip sempre tem os \_ estilos de janela pop-up WS e WS \_ ex \_ TOOLWINDOW, independentemente de você especificá-los ao criar o controle.</span><span class="sxs-lookup"><span data-stu-id="5744d-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5744d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5744d-133">Requirements</span></span>



| <span data-ttu-id="5744d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5744d-134">Requirement</span></span> | <span data-ttu-id="5744d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5744d-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5744d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5744d-136">Header</span></span><br/> | <dl> <span data-ttu-id="5744d-137"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5744d-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





