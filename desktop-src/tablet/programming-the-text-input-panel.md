---
description: A partir do Windows Vista, o TextInputPanel substitui o PenInputPanel para controlar a aparência e o comportamento da tela do painel de entrada do Tablet. as seções a seguir descrevem a programação do painel de entrada usando as interfaces de programação de aplicativo do painel de entrada de texto. TextInputPanel para usuários do painel de entrada do PenInputPanelUsing AutoCompleteEnabling correção de texto para tinta personalizada CollectorsNote o painel de entrada de texto é implementado em um arquivo executável chamado TabTip.exe. A execução de TabTip.exe com o parâmetro/SeekDesktop tenta executar uma versão de funcionalidade reduzida do painel de entrada em uma área de trabalho interativa não padrão, conforme criado com createdesktop. Para as áreas de trabalho mais criadas, o painel de entrada será executado automaticamente nesse modo. Esse parâmetro fornece os meios para iniciá-lo em cenários de aplicativos incomuns que, caso contrário, impedem o lançamento automático. Se o painel de entrada já estiver em execução na área de trabalho, esse parâmetro não terá efeito e a instância do TabTip.exe será encerrada imediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programando o painel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785963"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="f49a6-107">Programando o painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="f49a6-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="f49a6-108">A partir do Windows Vista, o [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) substitui o [**PenInputPanel**](peninputpanel-class.md) para controlar a aparência e o comportamento da tela do painel de entrada do Tablet.</span><span class="sxs-lookup"><span data-stu-id="f49a6-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="f49a6-109">As seções a seguir descrevem a programação do painel de entrada usando as interfaces de programação de aplicativo do painel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="f49a6-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="f49a6-110">TextInputPanel para usuários de PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="f49a6-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="f49a6-111">Usando o preenchimento automático do painel de entrada</span><span class="sxs-lookup"><span data-stu-id="f49a6-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="f49a6-112">Habilitando a correção de texto para coletores de tinta personalizados</span><span class="sxs-lookup"><span data-stu-id="f49a6-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="f49a6-113">O painel de entrada de texto é implementado em um arquivo executável chamado TabTip.exe.</span><span class="sxs-lookup"><span data-stu-id="f49a6-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="f49a6-114">A execução de TabTip.exe com o parâmetro */SeekDesktop* tenta executar uma versão de funcionalidade reduzida do painel de entrada em uma área de trabalho interativa não padrão, conforme criado com [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="f49a6-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="f49a6-115">Para as áreas de trabalho mais criadas, o painel de entrada será executado automaticamente nesse modo.</span><span class="sxs-lookup"><span data-stu-id="f49a6-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="f49a6-116">Esse parâmetro fornece os meios para iniciá-lo em cenários de aplicativos incomuns que, caso contrário, impedem o lançamento automático.</span><span class="sxs-lookup"><span data-stu-id="f49a6-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="f49a6-117">Se o painel de entrada já estiver em execução na área de trabalho, esse parâmetro não terá efeito e a instância do TabTip.exe será encerrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f49a6-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f49a6-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f49a6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f49a6-119">Programando o painel de entrada usando a classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="f49a6-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
