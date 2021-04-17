---
title: TVN_ASYNCDRAW código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore para seu pai quando o desenho de um ícone ou sobreposição falhou. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748249"
---
# <a name="tvn_asyncdraw-notification-code"></a><span data-ttu-id="d639d-105">Código de notificação do TVN \_ ASYNCDRAW</span><span class="sxs-lookup"><span data-stu-id="d639d-105">TVN\_ASYNCDRAW notification code</span></span>

<span data-ttu-id="d639d-106">Enviado por um controle de exibição de árvore para seu pai quando o desenho de um ícone ou sobreposição falhou.</span><span class="sxs-lookup"><span data-stu-id="d639d-106">Sent by a tree-view control to its parent when the drawing of a icon or overlay has failed.</span></span> <span data-ttu-id="d639d-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d639d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d639d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d639d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d639d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d639d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d639d-110">Ponteiro para uma estrutura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="d639d-110">Pointer to an [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="d639d-111">A estrutura **NMTVASYNCDRAW** contém o motivo pelo qual o empate falhou.</span><span class="sxs-lookup"><span data-stu-id="d639d-111">The **NMTVASYNCDRAW** structure contains the reason the draw failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d639d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d639d-112">Return value</span></span>

<span data-ttu-id="d639d-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d639d-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d639d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d639d-114">Remarks</span></span>

<span data-ttu-id="d639d-115">O controle de exibição de árvore deve ter o estilo estendido de [**TVs \_ ex \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d639d-115">The tree-view control must have the [**TVS\_EX\_DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="d639d-116">Observe que isso é equivalente ao sinalizador LVN ASYNCDRAWN da exibição de lista \_ e seu estilo correspondente.</span><span class="sxs-lookup"><span data-stu-id="d639d-116">Note that this is equivalent to list-view's LVN\_ASYNCDRAWN flag and its corresponding style.</span></span>

<span data-ttu-id="d639d-117">Esse controle não é desenhado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d639d-117">This control does not draw asynchronously.</span></span> <span data-ttu-id="d639d-118">Assíncrona é usado no contexto que o controle de exibição de árvore não extrai de forma síncrona uma imagem se ela não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="d639d-118">Asynchronous is used in the context that the tree-view control does not synchronously extract an image if it is not available.</span></span> <span data-ttu-id="d639d-119">(Por exemplo, a imagem pode não estar disponível se o controle de exibição de árvore usar uma lista de imagens esparsas, uma vez que a imagem pode ser descarregada.) Em vez disso, quando uma imagem não está disponível, o controle, de forma síncrona, solicita ao pai qual ação tomar enviando o pai uma \_ notificação TVN ASYNCDRAW com uma estrutura [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) .</span><span class="sxs-lookup"><span data-stu-id="d639d-119">(For instance, the image may not be available if the tree-view control uses a sparse image list, since the image may be unloaded.) Instead, when an image is not available, the control synchronously asks the parent what action to take by sending the parent an TVN\_ASYNCDRAW notification with a [**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) structure.</span></span> <span data-ttu-id="d639d-120">O membro de **RH** desta estrutura descreve o motivo pelo qual o desenho do controle falhou.</span><span class="sxs-lookup"><span data-stu-id="d639d-120">The **hr** member of this structure describes the reason the control's draw failed.</span></span> <span data-ttu-id="d639d-121">Um resultado de **RH** de E \_ pendente significa que a imagem não está presente (a imagem precisa ser extraída).</span><span class="sxs-lookup"><span data-stu-id="d639d-121">An **hr** result of E\_PENDING means the image is not present at all (the image needs to be extracted).</span></span> <span data-ttu-id="d639d-122">Êxito indica que a imagem está presente, mas não na qualidade da imagem necessária.</span><span class="sxs-lookup"><span data-stu-id="d639d-122">Success indicates that the image is present but not at the required image quality.</span></span>

<span data-ttu-id="d639d-123">O pai define o membro **dwRetFlags** da estrutura para informar ao controle como proceder.</span><span class="sxs-lookup"><span data-stu-id="d639d-123">The parent sets the **dwRetFlags** member of the structure to inform the control how to proceed.</span></span> <span data-ttu-id="d639d-124">Por exemplo, o pai pode retornar outra imagem, no membro **iRetImageIndex** , para o controle desenhar.</span><span class="sxs-lookup"><span data-stu-id="d639d-124">For instance, the parent may return another image, in the **iRetImageIndex** member, for the control to draw.</span></span> <span data-ttu-id="d639d-125">Nesse caso, o pai define o membro **dwRetFlags** como ADRF \_ DRAWIMAGE.</span><span class="sxs-lookup"><span data-stu-id="d639d-125">In this case, the parent sets the **dwRetFlags** member to ADRF\_DRAWIMAGE.</span></span> <span data-ttu-id="d639d-126">Se o controle encontrar a imagem retornada não tiver sido extraído, ainda outra \_ notificação de ASYNCDRAW TVN poderá ser enviada pelo controle.</span><span class="sxs-lookup"><span data-stu-id="d639d-126">If the control finds the returned image has not been extracted, yet another TVN\_ASYNCDRAW notification may be sent by the control.</span></span>

<span data-ttu-id="d639d-127">Se uma imagem não estiver disponível, a ideia por trás da assíncrona é permitir que o pai faça a extração em segundo plano para que a extração não bloqueie o thread da interface do usuário, ou seja, o thread no qual o controle está.</span><span class="sxs-lookup"><span data-stu-id="d639d-127">If an image is not available, the idea behind asynchronous is to allow the parent do the extraction in the background so that extraction does not block the UI thread, that is, the thread the control is on.</span></span> <span data-ttu-id="d639d-128">O pai pode retornar ADRF \_ DRAWNOTHING ao controle e, em seguida, iniciar um thread em segundo plano para extrair o ícone.</span><span class="sxs-lookup"><span data-stu-id="d639d-128">The parent may return ADRF\_DRAWNOTHING to the control, then launch a background thread to extract the icon.</span></span> <span data-ttu-id="d639d-129">Depois de extraído, o pai pode definir o ícone no controle TreeView com macro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span><span class="sxs-lookup"><span data-stu-id="d639d-129">Once extracted, the parent may set the icon in the treeview control with macro [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem).</span></span> <span data-ttu-id="d639d-130">Isso faz com que a exibição de árvore invalidasse o item e, eventualmente, repinte-o com a imagem extraída na lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="d639d-130">This causes tree-view to invalidate the item and eventually repaint it with the extracted image in the image list.</span></span>

<span data-ttu-id="d639d-131">O exemplo de código a seguir, a ser usado como parte de um programa maior, mostra como um pai pode processar dois códigos de retorno possíveis nessa notificação por um controle e decidir qual ação deve ser tomada pelo controle.</span><span class="sxs-lookup"><span data-stu-id="d639d-131">The following code example, to be used as part of a larger program, shows how a parent may process two possible return codes in this notification by a control, and decide what action the control should take.</span></span> <span data-ttu-id="d639d-132">A configuração de **dwRetFlags** não é mostrada.</span><span class="sxs-lookup"><span data-stu-id="d639d-132">Setting **dwRetFlags** is not shown.</span></span>


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a><span data-ttu-id="d639d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d639d-133">Requirements</span></span>



| <span data-ttu-id="d639d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d639d-134">Requirement</span></span> | <span data-ttu-id="d639d-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d639d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d639d-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d639d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d639d-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d639d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d639d-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d639d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d639d-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d639d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d639d-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d639d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d639d-141"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d639d-141"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





