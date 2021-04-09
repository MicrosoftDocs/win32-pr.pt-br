---
title: Interfaces de condição de propriedade para clientes
description: Esta seção descreve as interfaces de condição de propriedade para clientes de automação da interface do usuário para aplicativos Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007637"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="2b76a-103">Interfaces de condição de propriedade para clientes</span><span class="sxs-lookup"><span data-stu-id="2b76a-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="2b76a-104">Esta seção descreve as interfaces de condição de propriedade para clientes de automação da interface do usuário para aplicativos Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="2b76a-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2b76a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2b76a-105">In this section</span></span>



| <span data-ttu-id="2b76a-106">Interface</span><span class="sxs-lookup"><span data-stu-id="2b76a-106">Interface</span></span>                                                                                  | <span data-ttu-id="2b76a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b76a-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b76a-108">**IUIAutomationAndCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="2b76a-109">Expõe as propriedades e os métodos que os aplicativos cliente de automação da interface do usuário da Microsoft podem usar para recuperar informações sobre uma condição de propriedade baseada em e.</span><span class="sxs-lookup"><span data-stu-id="2b76a-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="2b76a-110">**IUIAutomationBoolCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="2b76a-111">Representa uma condição que pode ser **true** (seleciona todos os elementos) ou **false** (não seleciona nenhum elemento).</span><span class="sxs-lookup"><span data-stu-id="2b76a-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="2b76a-112">**IUIAutomationCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="2b76a-113">Essa é a interface principal para condições usadas na filtragem ao Pesquisar elementos na árvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b76a-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="2b76a-114">**IUIAutomationNotCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="2b76a-115">Representa uma condição que é negativa de outra condição.</span><span class="sxs-lookup"><span data-stu-id="2b76a-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2b76a-116">**IUIAutomationOrCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="2b76a-117">Representa uma condição composta por várias condições, pelo menos uma das quais deve ser verdadeira.</span><span class="sxs-lookup"><span data-stu-id="2b76a-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="2b76a-118">**IUIAutomationPropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="2b76a-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="2b76a-119">Representa uma condição baseada em um valor de propriedade que é usado para localizar elementos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="2b76a-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="2b76a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b76a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b76a-121">Clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="2b76a-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

