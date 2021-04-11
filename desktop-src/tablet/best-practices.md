---
description: Visão geral das práticas recomendadas ao usar o objeto do painel de entrada da caneta.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Práticas recomendadas (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172068"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="edc14-103">Práticas recomendadas (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="edc14-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="edc14-104">Há algumas diretrizes para ter em mente ao usar o objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="edc14-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="edc14-105">Preferir o controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="edc14-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="edc14-106">Desabilitar modo de tinta em controles InkEdit</span><span class="sxs-lookup"><span data-stu-id="edc14-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="edc14-107">Usando controles sem janela</span><span class="sxs-lookup"><span data-stu-id="edc14-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="edc14-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edc14-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="edc14-109">Preferir o controle InkEdit</span><span class="sxs-lookup"><span data-stu-id="edc14-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="edc14-110">[InkEdit](inkedit-control-reference.md) é o controle preferencial ao qual anexar o objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="edc14-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="edc14-111">O controle InkEdit fornece suporte para a [TSF (estrutura de serviços de texto)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="edc14-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="edc14-112">Desabilitar modo de tinta em controles InkEdit</span><span class="sxs-lookup"><span data-stu-id="edc14-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="edc14-113">Quando anexado a um controle [InkEdit](inkedit-control-reference.md) , defina a propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) do controle InkEdit como o valor [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) .</span><span class="sxs-lookup"><span data-stu-id="edc14-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="edc14-114">Se a propriedade **InkMode** não estiver definida como o valor de **InkMode** , o controle InkEdit interpretará o primeiro toque como um traço, o passará para o reconhecedor e inserirá o texto no controle InkEdit.</span><span class="sxs-lookup"><span data-stu-id="edc14-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="edc14-115">Como você já tem um objeto [**PenInputPanel**](peninputpanel-class.md) anexado para aceitar entrada à tinta, não é necessário ter o controle InkEdit também habilitado para entrada à tinta.</span><span class="sxs-lookup"><span data-stu-id="edc14-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="edc14-116">Usando controles sem janela</span><span class="sxs-lookup"><span data-stu-id="edc14-116">Using Windowless Controls</span></span>

<span data-ttu-id="edc14-117">Quando um objeto [**PenInputPanel**](peninputpanel-class.md) é anexado a uma janela pai que contém mais de um controle sem janela, o objeto **PenInputPanel** não sabe como controlar o cursor como o foco se move entre os filhos sem janelas.</span><span class="sxs-lookup"><span data-stu-id="edc14-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="edc14-118">A entrada de manuscrito pode ser enviada para o filho incorreto quando o foco é movido de um controle sem janela para outro enquanto a entrada está pendente.</span><span class="sxs-lookup"><span data-stu-id="edc14-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="edc14-119">Para usar o objeto [**PenInputPanel**](peninputpanel-class.md) em um ambiente sem janelas, a técnica a seguir pode ser usada:</span><span class="sxs-lookup"><span data-stu-id="edc14-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="edc14-120">Crie uma instância de um controle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) e posicione-o sobre o controle sem janela.</span><span class="sxs-lookup"><span data-stu-id="edc14-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="edc14-121">Anexe o objeto [**PenInputPanel**](peninputpanel-class.md) ao novo controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="edc14-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="edc14-122">Deixe o controle de caixa de texto coletar o texto reconhecido do objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="edc14-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="edc14-123">Quando o foco é alterado para fora do controle de caixa de texto, chame o método [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) do objeto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="edc14-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="edc14-124">Copie o texto reconhecido do controle caixa de texto para o filho sem janela.</span><span class="sxs-lookup"><span data-stu-id="edc14-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="edc14-125">Desanexe o objeto [**PenInputPanel**](peninputpanel-class.md) definindo sua propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (código gerenciado somente) ou a propriedade [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) como NULL.</span><span class="sxs-lookup"><span data-stu-id="edc14-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="edc14-126">Destrua o controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="edc14-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="edc14-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edc14-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edc14-128">**Classe PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="edc14-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="edc14-129">[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="edc14-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="edc14-130">Estrutura de serviços de texto</span><span class="sxs-lookup"><span data-stu-id="edc14-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
