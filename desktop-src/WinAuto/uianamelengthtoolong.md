---
title: UiaNameLengthTooLong
description: UiaNameLengthTooLong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- UIA_NamePropertyId do identificador AutomationElement. NameProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364343"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="495bd-104">UiaNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="495bd-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="495bd-105">Texto</span><span class="sxs-lookup"><span data-stu-id="495bd-105">Text</span></span>

<span data-ttu-id="495bd-106">O nome do elemento não deve retornar uma cadeia de caracteres com mais de um {0} caractere</span><span class="sxs-lookup"><span data-stu-id="495bd-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="495bd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="495bd-107">Type</span></span>

<span data-ttu-id="495bd-108">Erro</span><span class="sxs-lookup"><span data-stu-id="495bd-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="495bd-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="495bd-109">Description</span></span>

<span data-ttu-id="495bd-110">O nome de um elemento contém muitos caracteres.</span><span class="sxs-lookup"><span data-stu-id="495bd-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="495bd-111">Por exemplo, o método [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) usado para recuperar o nome UIA de um elemento retorna uma cadeia de caracteres maior que o limite.</span><span class="sxs-lookup"><span data-stu-id="495bd-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="495bd-112">Esse problema causa problemas para as pessoas que contam com um leitor de tela e um teclado para navegação porque um elemento pode ter um nome não-pronunciado e não intuitivo.</span><span class="sxs-lookup"><span data-stu-id="495bd-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="495bd-113">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="495bd-113">Possible causes</span></span>

<span data-ttu-id="495bd-114">O elemento ou seu pai tem um nome ou rótulo atribuído incorretamente.</span><span class="sxs-lookup"><span data-stu-id="495bd-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="495bd-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="495bd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="495bd-116">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="495bd-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="495bd-117">**IUIAutomationElement:: CurrentName**</span><span class="sxs-lookup"><span data-stu-id="495bd-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




