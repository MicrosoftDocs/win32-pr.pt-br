---
title: Usando controles de guia
description: Este tópico contém dois exemplos que usam controles guia.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104454413"
---
# <a name="using-tab-controls"></a><span data-ttu-id="35fa9-103">Usando controles de guia</span><span class="sxs-lookup"><span data-stu-id="35fa9-103">Using Tab Controls</span></span>

<span data-ttu-id="35fa9-104">Este tópico contém dois exemplos que usam controles guia.</span><span class="sxs-lookup"><span data-stu-id="35fa9-104">This topic contains two examples that use tab controls.</span></span> <span data-ttu-id="35fa9-105">O primeiro exemplo demonstra como usar um controle guia para alternar entre várias páginas de texto na janela principal de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35fa9-105">The first example demonstrates how to use a tab control to switch between multiple pages of text in an application's main window.</span></span> <span data-ttu-id="35fa9-106">O segundo exemplo demonstra como usar um controle guia para alternar entre várias páginas de controles em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35fa9-106">The second example demonstrates how to use a tab control to switch between multiple pages of controls in a dialog box.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35fa9-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="35fa9-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35fa9-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="35fa9-108">Topic</span></span></th>
<th><span data-ttu-id="35fa9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="35fa9-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35fa9-110"><a href="create-a-tab-control-in-the-main-window.md">Como criar um controle guia na janela principal</a></span><span class="sxs-lookup"><span data-stu-id="35fa9-110"><a href="create-a-tab-control-in-the-main-window.md">How to Create a Tab Control in the Main Window</a></span></span><br/></td>
<td><span data-ttu-id="35fa9-111">O exemplo nesta seção demonstra como criar um controle guia e exibi-lo na área cliente da janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35fa9-111">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="35fa9-112">O aplicativo exibe uma terceira janela (um controle estático) na área de exibição do controle guia.</span><span class="sxs-lookup"><span data-stu-id="35fa9-112">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="35fa9-113">A janela pai posiciona e dimensiona o controle de tabulação e o controle estático ao processar a mensagem de <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="35fa9-113">The parent window positions and sizes the tab control and static control when it processes the <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> message.</span></span> <br/> <span data-ttu-id="35fa9-114">Há sete guias neste exemplo, uma para cada dia da semana.</span><span class="sxs-lookup"><span data-stu-id="35fa9-114">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="35fa9-115">Quando o usuário seleciona uma guia, o aplicativo exibe o nome do dia correspondente no controle estático.</span><span class="sxs-lookup"><span data-stu-id="35fa9-115">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35fa9-116"><a href="create-a-tabbed-dialog-box.md">Como criar uma caixa de diálogo com guias</a></span><span class="sxs-lookup"><span data-stu-id="35fa9-116"><a href="create-a-tabbed-dialog-box.md">How to Create a Tabbed Dialog Box</a></span></span><br/></td>
<td><span data-ttu-id="35fa9-117">O exemplo nesta seção demonstra como criar uma caixa de diálogo que usa guias para fornecer várias páginas de controles.</span><span class="sxs-lookup"><span data-stu-id="35fa9-117">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="35fa9-118">A caixa de diálogo principal é uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="35fa9-118">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="35fa9-119">Cada página de controles é definida por um modelo de caixa de diálogo que tem o estilo de <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="35fa9-119">Each page of controls is defined by a dialog box template that has the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> style.</span></span> <span data-ttu-id="35fa9-120">Quando uma guia é selecionada, uma caixa de diálogo sem janela restrita é criada para a página de entrada e a caixa de diálogo da página de saída é destruída.</span><span class="sxs-lookup"><span data-stu-id="35fa9-120">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="35fa9-121">Em muitos casos, você pode implementar caixas de diálogo de várias páginas com mais facilidade usando folhas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="35fa9-121">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="35fa9-122">Para obter mais informações sobre folhas de propriedades, consulte <a href="property-sheets.md">about Property Sheets</a>.</span><span class="sxs-lookup"><span data-stu-id="35fa9-122">For more information about property sheets, see <a href="property-sheets.md">About Property Sheets</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="35fa9-123">O modelo da caixa de diálogo principal simplesmente define dois controles Button.</span><span class="sxs-lookup"><span data-stu-id="35fa9-123">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="35fa9-124">Ao processar a mensagem de <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , o procedimento da caixa de diálogo cria um controle guia e carrega os recursos de modelo da caixa de diálogo para cada uma das caixas de diálogo filhas.</span><span class="sxs-lookup"><span data-stu-id="35fa9-124">When processing the <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

