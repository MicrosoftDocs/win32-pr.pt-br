---
description: Uma caixa de diálogo de erro é uma caixa de diálogo modal que exibe uma mensagem de erro. Mais de uma caixa de diálogo de erro pode existir em cada instalação.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Diálogo de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502055"
---
# <a name="error-dialog"></a><span data-ttu-id="4fd6d-104">Diálogo de erro</span><span class="sxs-lookup"><span data-stu-id="4fd6d-104">Error Dialog</span></span>

<span data-ttu-id="4fd6d-105">Uma caixa de diálogo de erro é uma caixa de diálogo modal que exibe uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="4fd6d-106">Mais de uma caixa de diálogo de erro pode existir em cada instalação.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="4fd6d-107">É necessário definir uma propriedade ErrorDialog que especifica qual caixa de diálogo deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="4fd6d-108">Se essa propriedade não for definida ou não apontar para uma caixa de diálogo de erro válida, as mensagens de erro não serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="4fd6d-109">Nesse caso, o erro é registrado apenas com um aviso sobre a caixa de diálogo ausente.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="4fd6d-110">Uma caixa de diálogo de erro deve ter o conjunto de [bits do estilo da caixa de diálogo de erro](error-dialog-style-bit.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd6d-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="4fd6d-111">A caixa de diálogo deve ter um [controle de texto](text-control.md) chamado ErrorText.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="4fd6d-112">O registro da caixa de diálogo de erro na [tabela de diálogo](dialog-table.md) deve ter o controle ErrorText inserido no \_ primeiro campo Control.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="4fd6d-113">A caixa de diálogo deve conter sete [Supressãos](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6d-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="4fd6d-114">Todos esses botões especificam o [EndDialog](enddialog-controlevent.md) ControlEvent, na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6d-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="4fd6d-115">Cada botão especifica um dos seguintes atributos: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="4fd6d-116">O foco desses controles não deve ser vinculado por meio do uso da \_ próxima coluna de controle na [tabela de controle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="4fd6d-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="4fd6d-117">Esses botões devem ser colocados em aproximadamente a mesma posição na caixa de diálogo porque, quando ele é criado, apenas um subconjunto desses sete botões é criado, dependendo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="4fd6d-118">A coordenada X dos botões é modificada para que os botões exibidos tenham espaçamento uniforme.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="4fd6d-119">A coordenada Y, a altura e a largura dos botões são inalteradas.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="4fd6d-120">Como os botões são organizados horizontalmente, nenhum outro controle pode ser colocado na mesma região horizontal da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="4fd6d-121">Para uma caixa de diálogo de erro, os campos de controle \_ padrão e de \_ cancelamento de controle na [tabela de diálogo](dialog-table.md) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="4fd6d-122">O \_ primeiro campo controlar para uma caixa de diálogo de erro deve especificar o controle ErrorText.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="4fd6d-123">Se um [controle de ícone](icon-control.md) chamado ErrorIcon estiver incluído nessa caixa de diálogo, os seguintes ícones padrão do Windows serão exibidos:</span><span class="sxs-lookup"><span data-stu-id="4fd6d-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="4fd6d-124">\_Erro de Idi em resposta a mensagens imtFatalExit.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="4fd6d-125">IDI \_ aviso em resposta às mensagens imtError e imtWarning.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="4fd6d-126">IDI \_ informações em resposta a mensagens imtOutOfDiskSpace.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="4fd6d-127">O controle ErrorIcon deve ser criado com o [atributo de controle FixedSize](fixedsize-control-attribute.md) definido para evitar o dimensionamento impróprio dos ícones padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="4fd6d-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 



