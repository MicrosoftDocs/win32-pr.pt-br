---
title: Estruturas de automação da interface do usuário
description: Esta seção descreve as estruturas usadas pelos aplicativos cliente de automação da interface do usuário e pelo provedor de automação da interface do usuário do Microsoft Win32.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453543"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="6bf4a-103">Estruturas de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="6bf4a-103">UI Automation Structures</span></span>

<span data-ttu-id="6bf4a-104">Esta seção descreve as estruturas usadas pelos aplicativos cliente de automação da interface do usuário e pelo provedor de automação da interface do usuário do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6bf4a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="6bf4a-105">In this section</span></span>



| <span data-ttu-id="6bf4a-106">Estrutura</span><span class="sxs-lookup"><span data-stu-id="6bf4a-106">Structure</span></span>                                                                            | <span data-ttu-id="6bf4a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bf4a-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6bf4a-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="6bf4a-109">Contém informações sobre uma propriedade estendida.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="6bf4a-110">**UIAutomationEventInfo**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="6bf4a-111">Contém informações sobre um evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="6bf4a-112">**UIAutomationMethodInfo**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="6bf4a-113">Contém informações sobre um método que é suportado por um padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="6bf4a-114">**UIAutomationParameter**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="6bf4a-115">Contém informações sobre um parâmetro de um padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="6bf4a-116">**UIAutomationPatternInfo**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="6bf4a-117">Contém informações sobre um padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="6bf4a-118">**UIAutomationPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="6bf4a-119">Contém informações sobre uma propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="6bf4a-120">**UiaChangeInfo**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="6bf4a-121">Contém dados sobre uma alteração de automação de interface do usuário que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="6bf4a-122">**UiaPoint**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="6bf4a-123">Contém as coordenadas de um ponto.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="6bf4a-124">**UiaRect**</span><span class="sxs-lookup"><span data-stu-id="6bf4a-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="6bf4a-125">Contém a posição e o tamanho de um retângulo, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="6bf4a-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





