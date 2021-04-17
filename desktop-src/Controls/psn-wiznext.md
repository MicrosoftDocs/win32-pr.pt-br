---
title: PSN_WIZNEXT código de notificação (Prsht. h)
description: Notifica uma página que o usuário clicou no botão Avançar em um assistente. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749074"
---
# <a name="psn_wiznext-notification-code"></a><span data-ttu-id="15d7a-105">Código de notificação do PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="15d7a-105">PSN\_WIZNEXT notification code</span></span>

<span data-ttu-id="15d7a-106">Notifica uma página que o usuário clicou no botão **Avançar** em um assistente.</span><span class="sxs-lookup"><span data-stu-id="15d7a-106">Notifies a page that the user has clicked the **Next** button in a wizard.</span></span> <span data-ttu-id="15d7a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="15d7a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="15d7a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15d7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15d7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15d7a-110">Ponteiro para uma estrutura [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="15d7a-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="15d7a-111">Essa estrutura contém uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) como seu primeiro membro, **HDR**. O membro **hwndFrom** dessa estrutura **NMHDR** contém o identificador para a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="15d7a-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="15d7a-112">O membro **lParam** da estrutura **PSHNOTIFY** não contém nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="15d7a-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d7a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15d7a-113">Return value</span></span>

<span data-ttu-id="15d7a-114">Retorne 0 para permitir que o assistente vá para a próxima página.</span><span class="sxs-lookup"><span data-stu-id="15d7a-114">Return 0 to allow the wizard to go to the next page.</span></span> <span data-ttu-id="15d7a-115">Retorne-1 para impedir que o assistente altere as páginas.</span><span class="sxs-lookup"><span data-stu-id="15d7a-115">Return -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="15d7a-116">Para exibir uma página específica, retorne seu identificador de recurso de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15d7a-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="15d7a-117">Se a caixa de diálogo tiver sido especificada com o sinalizador [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) , essa notificação retornará o ponteiro para o modelo da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15d7a-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d7a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="15d7a-118">Remarks</span></span>

<span data-ttu-id="15d7a-119">Para definir o valor de retorno, o procedimento da caixa de diálogo para a página deve chamar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o valor **\_ MSGRESULT DWL** e retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="15d7a-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="15d7a-120">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="15d7a-120">For example:</span></span>

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> <span data-ttu-id="15d7a-121">A folha de propriedades está no processo de manipulação da lista de páginas quando o código de \_ notificação PSN WIZNEXT é enviado.</span><span class="sxs-lookup"><span data-stu-id="15d7a-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZNEXT notification code is sent.</span></span> <span data-ttu-id="15d7a-122">Você pode adicionar, inserir ou remover páginas em resposta a esses códigos de notificação, mas deve ser levado um cuidado especial se você inserir ou remover páginas antes da página atual.</span><span class="sxs-lookup"><span data-stu-id="15d7a-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="15d7a-123">Se você inserir ou remover páginas antes da página atual, deverá retornar (por meio de **DWL \_ MSGRESULT**) um valor diferente de zero para especificar a página nova desejada.</span><span class="sxs-lookup"><span data-stu-id="15d7a-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="15d7a-124">No entanto, observe que se você inserir ou remover uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.</span><span class="sxs-lookup"><span data-stu-id="15d7a-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="15d7a-125">Por esse motivo, é recomendável que os assistentes que adicionam e removem páginas dinamicamente em resposta a PSN \_ WIZNEXT e [PSN \_ WIZBACK](psn-wizback.md) façam isso somente para páginas no final da lista.</span><span class="sxs-lookup"><span data-stu-id="15d7a-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to PSN\_WIZNEXT and [PSN\_WIZBACK](psn-wizback.md) do so only to pages at the end of the list.</span></span> <span data-ttu-id="15d7a-126">Se você quiser que o assistente remova as páginas com precisão, mantenha as páginas dinâmicas no final da lista e volte para páginas permanentes antes de excluí-las.</span><span class="sxs-lookup"><span data-stu-id="15d7a-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="15d7a-127">Por exemplo, suponha que um assistente consiste em uma página introdutória, uma série de páginas dinâmicas e uma página de conclusão, e você deseja excluir as páginas dinâmicas quando o usuário atingir a página de conclusão.</span><span class="sxs-lookup"><span data-stu-id="15d7a-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="15d7a-128">O assistente começaria com duas páginas, "introdução" e "conclusão".</span><span class="sxs-lookup"><span data-stu-id="15d7a-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="15d7a-129">O usuário começa na página "introdução".</span><span class="sxs-lookup"><span data-stu-id="15d7a-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="15d7a-130">Introdução (o usuário está aqui)</span><span class="sxs-lookup"><span data-stu-id="15d7a-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="15d7a-131">Completion</span><span class="sxs-lookup"><span data-stu-id="15d7a-131">Completion</span></span>
2.  <span data-ttu-id="15d7a-132">Quando o usuário sai da "introdução", o assistente adiciona as páginas dinâmicas e coloca o usuário na primeira página dinâmica retornando (por meio de **DWL \_ MSGRESULT**) o identificador da caixa de diálogo da página "dinâmico 1".</span><span class="sxs-lookup"><span data-stu-id="15d7a-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="15d7a-133">Neste exemplo, há três páginas dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="15d7a-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="15d7a-134">Introdução</span><span class="sxs-lookup"><span data-stu-id="15d7a-134">Introduction</span></span>
    2.  <span data-ttu-id="15d7a-135">Completion</span><span class="sxs-lookup"><span data-stu-id="15d7a-135">Completion</span></span>
    3.  <span data-ttu-id="15d7a-136">Dinâmico 1 (o usuário está aqui)</span><span class="sxs-lookup"><span data-stu-id="15d7a-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="15d7a-137">Dinâmico 2</span><span class="sxs-lookup"><span data-stu-id="15d7a-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="15d7a-138">Dinâmico 3</span><span class="sxs-lookup"><span data-stu-id="15d7a-138">Dynamic 3</span></span>
3.  <span data-ttu-id="15d7a-139">Depois que o usuário navega pelas páginas dinâmicas para "Dynamic 3" e, em seguida, navega para a próxima página, o aplicativo deve posicionar o usuário na página "conclusão".</span><span class="sxs-lookup"><span data-stu-id="15d7a-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="15d7a-140">Novamente, isso é feito retornando (por meio de **DWL \_ MSGRESULT**) o identificador da caixa de diálogo da página "conclusão".</span><span class="sxs-lookup"><span data-stu-id="15d7a-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="15d7a-141">Introdução</span><span class="sxs-lookup"><span data-stu-id="15d7a-141">Introduction</span></span>
    2.  <span data-ttu-id="15d7a-142">Conclusão (o usuário está aqui)</span><span class="sxs-lookup"><span data-stu-id="15d7a-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="15d7a-143">Dinâmico 1</span><span class="sxs-lookup"><span data-stu-id="15d7a-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="15d7a-144">Dinâmico 2</span><span class="sxs-lookup"><span data-stu-id="15d7a-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="15d7a-145">Dinâmico 3</span><span class="sxs-lookup"><span data-stu-id="15d7a-145">Dynamic 3</span></span>
4.  <span data-ttu-id="15d7a-146">O aplicativo pode, então, remover as três páginas dinâmicas (numeradas de três a cinco) com segurança.</span><span class="sxs-lookup"><span data-stu-id="15d7a-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="15d7a-147">Introdução</span><span class="sxs-lookup"><span data-stu-id="15d7a-147">Introduction</span></span>
    2.  <span data-ttu-id="15d7a-148">Conclusão (o usuário está aqui)</span><span class="sxs-lookup"><span data-stu-id="15d7a-148">Completion (User is here)</span></span>

<span data-ttu-id="15d7a-149">Observe que essa técnica será necessária apenas se o assistente remover as páginas dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="15d7a-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="15d7a-150">Se o assistente Adicionar apenas páginas dinamicamente, esse processo não será necessário.</span><span class="sxs-lookup"><span data-stu-id="15d7a-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d7a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d7a-151">Requirements</span></span>



| <span data-ttu-id="15d7a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d7a-152">Requirement</span></span> | <span data-ttu-id="15d7a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="15d7a-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15d7a-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15d7a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="15d7a-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15d7a-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15d7a-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15d7a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="15d7a-157">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15d7a-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15d7a-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15d7a-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="15d7a-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d7a-159"><dt>Prsht.h</dt></span></span> </dl> |



 

