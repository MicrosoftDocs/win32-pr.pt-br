---
title: Estilos de controle SysLink (CommCtrl. h)
description: As constantes de estilo a seguir são usadas ao criar controles SysLink.
ms.assetid: e9a8c99b-86c4-4385-ae20-b2b78a07b491
topic_type:
- apiref
api_name:
- LWS_TRANSPARENT
- LWS_IGNORERETURN
- LWS_NOPREFIX
- LWS_USEVISUALSTYLE
- LWS_USECUSTOMTEXT
- LWS_RIGHT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 490a64a21ec81c1c91cc34ec8bebd2995476db4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748934"
---
# <a name="syslink-control-styles"></a><span data-ttu-id="38ea0-103">Estilos de controle SysLink</span><span class="sxs-lookup"><span data-stu-id="38ea0-103">SysLink Control Styles</span></span>

<span data-ttu-id="38ea0-104">As constantes de estilo a seguir são usadas ao criar controles SysLink.</span><span class="sxs-lookup"><span data-stu-id="38ea0-104">The following style constants are used when creating SysLink controls.</span></span>



| <span data-ttu-id="38ea0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="38ea0-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="38ea0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="38ea0-106">Description</span></span>                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LWS_TRANSPARENT"></span><span id="lws_transparent"></span><dl> <span data-ttu-id="38ea0-107"><dt>**transparente de LWS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-107"><dt>**LWS\_TRANSPARENT**</dt></span></span> </dl>             | <span data-ttu-id="38ea0-108">O modo de combinação em segundo plano é transparente.</span><span class="sxs-lookup"><span data-stu-id="38ea0-108">The background mix mode is transparent.</span></span> <br/>                                                                                                                       |
| <span id="LWS_IGNORERETURN_"></span><span id="lws_ignorereturn_"></span><dl> <span data-ttu-id="38ea0-109"><dt>**LWS \_ IGNORERETURN**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-109"><dt>**LWS\_IGNORERETURN** </dt></span></span> </dl>       | <span data-ttu-id="38ea0-110">Quando o link tem o foco do teclado e o usuário pressiona ENTER, o pressionamento de tecla é ignorado pelo controle e passado para a caixa de diálogo host.</span><span class="sxs-lookup"><span data-stu-id="38ea0-110">When the link has keyboard focus and the user presses Enter, the keystroke is ignored by the control and passed to the host dialog box.</span></span><br/>                        |
| <span id="LWS_NOPREFIX"></span><span id="lws_noprefix"></span><dl> <span data-ttu-id="38ea0-111"><dt>**LWS \_ NOprefix**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-111"><dt>**LWS\_NOPREFIX**</dt></span></span> </dl>                      | <span data-ttu-id="38ea0-112">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="38ea0-112">**Windows Vista**.</span></span> <span data-ttu-id="38ea0-113">Se o texto contiver um e comercial, ele será tratado como um caractere literal em vez do prefixo para uma tecla de atalho.</span><span class="sxs-lookup"><span data-stu-id="38ea0-113">If the text contains an ampersand, it is treated as a literal character rather than the prefix to a shortcut key.</span></span><br/>                           |
| <span id="LWS_USEVISUALSTYLE_"></span><span id="lws_usevisualstyle_"></span><dl> <span data-ttu-id="38ea0-114"><dt>**LWS \_ USEVISUALSTYLE**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-114"><dt>**LWS\_USEVISUALSTYLE** </dt></span></span> </dl> | <span data-ttu-id="38ea0-115">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="38ea0-115">**Windows Vista**.</span></span> <span data-ttu-id="38ea0-116">O link é exibido no estilo visual atual.</span><span class="sxs-lookup"><span data-stu-id="38ea0-116">The link is displayed in the current visual style.</span></span><br/>                                                                                          |
| <span id="LWS_USECUSTOMTEXT"></span><span id="lws_usecustomtext"></span><dl> <span data-ttu-id="38ea0-117"><dt>**USECUSTOMTEXT do LWS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-117"><dt>**LWS\_USECUSTOMTEXT**</dt></span></span> </dl>       | <span data-ttu-id="38ea0-118">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="38ea0-118">**Windows Vista**.</span></span> <span data-ttu-id="38ea0-119">Uma notificação [nm \_ CUSTOMTEXT](nm-customtext.md) é enviada quando o controle é desenhado, para que o aplicativo possa fornecer texto dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="38ea0-119">An [NM\_CUSTOMTEXT](nm-customtext.md) notification is sent when the control is drawn, so that the application can supply text dynamically.</span></span><br/> |
| <span id="LWS_RIGHT"></span><span id="lws_right"></span><dl> <span data-ttu-id="38ea0-120"><dt>**LWS \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-120"><dt>**LWS\_RIGHT**</dt></span></span> </dl>                               | <span data-ttu-id="38ea0-121">**Windows Vista**.</span><span class="sxs-lookup"><span data-stu-id="38ea0-121">**Windows Vista**.</span></span> <span data-ttu-id="38ea0-122">O texto é justificado à direita.</span><span class="sxs-lookup"><span data-stu-id="38ea0-122">The text is right-justified.</span></span><br/>                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="38ea0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ea0-123">Requirements</span></span>



| <span data-ttu-id="38ea0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ea0-124">Requirement</span></span> | <span data-ttu-id="38ea0-125">Valor</span><span class="sxs-lookup"><span data-stu-id="38ea0-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38ea0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38ea0-126">Header</span></span><br/> | <dl> <span data-ttu-id="38ea0-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38ea0-127"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





