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
# <a name="property-condition-interfaces-for-clients"></a>Interfaces de condição de propriedade para clientes

Esta seção descreve as interfaces de condição de propriedade para clientes de automação da interface do usuário para aplicativos Microsoft Win32.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                                  | Descrição                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Expõe as propriedades e os métodos que os aplicativos cliente de automação da interface do usuário da Microsoft podem usar para recuperar informações sobre uma condição de propriedade baseada em e. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Representa uma condição que pode ser **true** (seleciona todos os elementos) ou **false** (não seleciona nenhum elemento).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Essa é a interface principal para condições usadas na filtragem ao Pesquisar elementos na árvore de automação da interface do usuário.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Representa uma condição que é negativa de outra condição.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Representa uma condição composta por várias condições, pelo menos uma das quais deve ser verdadeira.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Representa uma condição baseada em um valor de propriedade que é usado para localizar elementos de automação da interface do usuário.<br/>                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de automação da interface do usuário](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

