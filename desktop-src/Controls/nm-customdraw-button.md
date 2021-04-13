---
title: Código de notificação de NM_CUSTOMDRAW (botão) (commctrl. h)
description: Notifica a janela pai de um controle de botão sobre as operações de desenho personalizadas no botão. O controle de botão envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Código de notificação de NM_CUSTOMDRAW (botão) controles do Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456049"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="3294b-105">\_Código de notificação nm CUSTOMDRAW (botão)</span><span class="sxs-lookup"><span data-stu-id="3294b-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="3294b-106">Notifica a janela pai de um controle de botão sobre as operações de desenho personalizadas no botão.</span><span class="sxs-lookup"><span data-stu-id="3294b-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="3294b-107">O controle de botão envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3294b-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3294b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3294b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3294b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3294b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3294b-110">Um ponteiro para uma estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) que contém informações sobre a operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="3294b-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="3294b-111">O membro **dwItemSpec** dessa estrutura contém o índice do item que está sendo desenhado e o membro **lItemlParam** dessa estrutura contém o *lParam* do item.</span><span class="sxs-lookup"><span data-stu-id="3294b-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3294b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3294b-112">Return value</span></span>

<span data-ttu-id="3294b-113">O valor que seu aplicativo pode retornar depende do estágio de desenho atual.</span><span class="sxs-lookup"><span data-stu-id="3294b-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="3294b-114">O membro **dwDrawStage** da estrutura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associada contém um valor que especifica o estágio de desenho.</span><span class="sxs-lookup"><span data-stu-id="3294b-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="3294b-115">Você deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3294b-115">You must return one of the following values.</span></span>



| <span data-ttu-id="3294b-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3294b-116">Return code</span></span>                                                                                          | <span data-ttu-id="3294b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3294b-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3294b-118"><dt>**CDRF \_ NOTIFYPOSTERASE**</dt></span><span class="sxs-lookup"><span data-stu-id="3294b-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="3294b-119">O controle notificará o pai depois de apagar um item.</span><span class="sxs-lookup"><span data-stu-id="3294b-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="3294b-120">Isso só poderá ser usado se **dwDrawStage** for igual a CDDs \_ preerase.</span><span class="sxs-lookup"><span data-stu-id="3294b-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="3294b-121"><dt>**CDRF \_ NOTIFYPOSTPAINT**</dt></span><span class="sxs-lookup"><span data-stu-id="3294b-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="3294b-122">O controle notificará o pai depois de pintar um item.</span><span class="sxs-lookup"><span data-stu-id="3294b-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="3294b-123">Isso pode ser usado somente se **dwDrawStage** for igual a CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="3294b-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3294b-124"><dt>**CDRF \_ SKIPDEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="3294b-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="3294b-125">O aplicativo desenhou o item manualmente.</span><span class="sxs-lookup"><span data-stu-id="3294b-125">The application drew the item manually.</span></span> <span data-ttu-id="3294b-126">O controle não vai desenhar o item.</span><span class="sxs-lookup"><span data-stu-id="3294b-126">The control will not draw the item.</span></span> <span data-ttu-id="3294b-127">Isso pode ser usado quando **dwDrawStage** é igual a CDDs \_ PREerase ou CDDs \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="3294b-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3294b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3294b-128">Remarks</span></span>

<span data-ttu-id="3294b-129">Se o controle de botão estiver marcado como OwnerDraw (BS \_ OwnerDraw), o \_ código de notificação nm CUSTOMDRAW não será enviado.</span><span class="sxs-lookup"><span data-stu-id="3294b-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="3294b-130">Consulte [usando o desenho personalizado](custom-draw.md) para mais discussões.</span><span class="sxs-lookup"><span data-stu-id="3294b-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="3294b-131">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3294b-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3294b-132">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3294b-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3294b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3294b-133">Requirements</span></span>



| <span data-ttu-id="3294b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3294b-134">Requirement</span></span> | <span data-ttu-id="3294b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3294b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3294b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3294b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3294b-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3294b-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3294b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3294b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3294b-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3294b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3294b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3294b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3294b-141"><dt>Commctrl. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3294b-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





