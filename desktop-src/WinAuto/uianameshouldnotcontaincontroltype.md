---
title: UiaNameShouldNotContainControlType
description: UiaNameShouldNotContainControlType
ms.assetid: 96F7A5FC-1879-4706-9E67-5B43D57F7281
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6178ca4cd4c4b2ed0deb0070116b597ba3bd1bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822479"
---
# <a name="uianameshouldnotcontaincontroltype"></a><span data-ttu-id="3d15f-103">UiaNameShouldNotContainControlType</span><span class="sxs-lookup"><span data-stu-id="3d15f-103">UiaNameShouldNotContainControlType</span></span>

## <a name="text"></a><span data-ttu-id="3d15f-104">Texto</span><span class="sxs-lookup"><span data-stu-id="3d15f-104">Text</span></span>

<span data-ttu-id="3d15f-105">O nome do elemento ( {0} ) não deve conter o texto do ControlType ( {1} )</span><span class="sxs-lookup"><span data-stu-id="3d15f-105">Element's Name ({0}) should not contain the text of the ControlType ({1})</span></span>

## <a name="type"></a><span data-ttu-id="3d15f-106">Type</span><span class="sxs-lookup"><span data-stu-id="3d15f-106">Type</span></span>

<span data-ttu-id="3d15f-107">Aviso</span><span class="sxs-lookup"><span data-stu-id="3d15f-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="3d15f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d15f-108">Description</span></span>

<span data-ttu-id="3d15f-109">O nome de um elemento incorpora seu tipo de controle UIA.</span><span class="sxs-lookup"><span data-stu-id="3d15f-109">The name of an element incorporates its UIA control type.</span></span> <span data-ttu-id="3d15f-110">Por exemplo, esse aviso pode ocorrer se a propriedade de nome UIA de um elemento com o tipo de controle de botão estiver definida como "meu botão".</span><span class="sxs-lookup"><span data-stu-id="3d15f-110">For example, this warning can occur if the UIA Name property for an element with the Button control type is set to "My Button".</span></span>

<span data-ttu-id="3d15f-111">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque o tipo de controle será lido duas vezes ou pode ser inpronunciado ou não intuitivo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="3d15f-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the control type will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="3d15f-112">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="3d15f-112">Possible causes</span></span>

-   <span data-ttu-id="3d15f-113">O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="3d15f-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="3d15f-114">O elemento ou seu pai tem um nome padrão que não foi revisado para um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="3d15f-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="3d15f-115">Por exemplo, Button1.</span><span class="sxs-lookup"><span data-stu-id="3d15f-115">For example, button1.</span></span>
-   <span data-ttu-id="3d15f-116">Um desenvolvedor não está ciente de que leitores de tela lêem nomes e tipos de controle.</span><span class="sxs-lookup"><span data-stu-id="3d15f-116">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d15f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d15f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d15f-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3d15f-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="3d15f-119">**IUIAutomationElement:: CurrentName**</span><span class="sxs-lookup"><span data-stu-id="3d15f-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




