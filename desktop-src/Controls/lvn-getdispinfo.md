---
title: LVN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista para sua janela pai. É uma solicitação para que a janela pai forneça as informações necessárias para exibir ou classificar um item de exibição de lista. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645275"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="648cc-106">Código de notificação do LVN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="648cc-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="648cc-107">Enviado por um controle de exibição de lista para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="648cc-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="648cc-108">É uma solicitação para que a janela pai forneça as informações necessárias para exibir ou classificar um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="648cc-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="648cc-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="648cc-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="648cc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="648cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="648cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="648cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="648cc-112">Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="648cc-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="648cc-113">Na entrada, a estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) contida nessa estrutura especifica o tipo de informação necessário e identifica o item ou subitem de interesse.</span><span class="sxs-lookup"><span data-stu-id="648cc-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="648cc-114">Use a estrutura **LVITEM** para retornar as informações solicitadas para o controle.</span><span class="sxs-lookup"><span data-stu-id="648cc-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="648cc-115">Se o manipulador de mensagens definir o \_ sinalizador LVIF di \_ SETITEM no membro **Mask** da estrutura **LVITEM** , o controle List-View armazenará as informações solicitadas e não solicitará novamente.</span><span class="sxs-lookup"><span data-stu-id="648cc-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="648cc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="648cc-116">Return value</span></span>

<span data-ttu-id="648cc-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="648cc-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="648cc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="648cc-118">Remarks</span></span>

<span data-ttu-id="648cc-119">O receptor de notificação converte *lParam* para recuperar a estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="648cc-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="648cc-120">O parâmetro *wParam* contém o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="648cc-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="648cc-121">Um controle de exibição de lista envia o código de notificação **LVN \_ GETDISPINFO** para recuperar informações de item armazenadas pelo aplicativo em vez do controle.</span><span class="sxs-lookup"><span data-stu-id="648cc-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="648cc-122">As informações podem ser informações de texto ou ícone de um item.</span><span class="sxs-lookup"><span data-stu-id="648cc-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="648cc-123">Ele também pode ser informações de estado do item.</span><span class="sxs-lookup"><span data-stu-id="648cc-123">It can also be item state information.</span></span> <span data-ttu-id="648cc-124">Consulte a mensagem [**LVM \_ SETCALLBACKMASK**](lvm-setcallbackmask.md) para obter mais informações sobre como implementar o estado do item em uma base de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="648cc-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="648cc-125">Para obter mais informações sobre retornos de chamada de exibição de lista, consulte [itens de retorno de chamada e a máscara de retorno de chamada](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="648cc-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="648cc-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="648cc-126">Examples</span></span>

<span data-ttu-id="648cc-127">O exemplo a seguir mostra como esse código de notificação pode ser tratado para definir o texto nas colunas de uma exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="648cc-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="648cc-128">Os dados de cada item são mantidos na estrutura a seguir.</span><span class="sxs-lookup"><span data-stu-id="648cc-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="648cc-129">O seguinte é do manipulador de \_ notificação do WM no procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="648cc-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="648cc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="648cc-130">Requirements</span></span>



| <span data-ttu-id="648cc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="648cc-131">Requirement</span></span> | <span data-ttu-id="648cc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="648cc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="648cc-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="648cc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="648cc-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="648cc-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="648cc-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="648cc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="648cc-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="648cc-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="648cc-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="648cc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="648cc-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="648cc-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="648cc-139">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="648cc-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="648cc-140">**LVN \_ GETDISPINFOW** (Unicode) e **LVN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="648cc-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="648cc-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="648cc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648cc-142">**LVN \_ SETDISPINFO**</span><span class="sxs-lookup"><span data-stu-id="648cc-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





