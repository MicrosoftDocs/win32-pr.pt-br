---
title: Interfaces de condição de propriedade para clientes
description: Esta seção descreve as interfaces de condição de propriedade Automação da Interface do Usuário clientes para aplicativos Microsoft Win32.
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447c2bf9a67a5fc9cbd303e86599502e2b6154f53485af5a57bf13a6268fa930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133479"
---
# <a name="property-condition-interfaces-for-clients"></a>Interfaces de condição de propriedade para clientes

Esta seção descreve as interfaces de condição de propriedade Automação da Interface do Usuário clientes para aplicativos Microsoft Win32.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                                  | Descrição                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationAndCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | Expõe propriedades e métodos que a Microsoft Automação da Interface do Usuário aplicativos cliente podem usar para recuperar informações sobre uma condição de propriedade baseada em AND. <br/> |
| [**IUIAutomationBoolCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | Representa uma condição que pode ser **TRUE** (seleciona todos os elementos) ou **FALSE** (não seleciona nenhum elemento).<br/>                                           |
| [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | Essa é a interface primária para condições usadas na filtragem ao pesquisar elementos na árvore Automação da Interface do Usuário dados.<br/>                                   |
| [**IUIAutomationNotCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | Representa uma condição que é o negativo de outra condição.<br/>                                                                                       |
| [**IUIAutomationOrCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | Representa uma condição com várias condições, pelo menos uma das quais deve ser verdadeira.<br/>                                                              |
| [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | Representa uma condição com base em um valor de propriedade usado para encontrar Automação da Interface do Usuário elementos.<br/>                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Automação da Interface do Usuário clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

