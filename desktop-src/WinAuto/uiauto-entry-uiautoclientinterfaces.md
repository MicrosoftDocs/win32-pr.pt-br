---
title: Interfaces de elementos de automação da interface do usuário para clientes
description: Esta seção descreve as interfaces usadas pelo cliente de automação da interface do usuário da Microsoft para localizar, acessar e consultar elementos de automação da interface do usuário.
ms.assetid: dd7cdcf1-3511-424f-b729-b71a7e11cdd8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356bd61a3f4a4626c8cc382c924b62967c01ddb201b8411eaa5451c822ede38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133409"
---
# <a name="ui-automation-element-interfaces-for-clients"></a>Interfaces de elementos de automação da interface do usuário para clientes

Esta seção descreve as interfaces usadas pelo cliente de automação da interface do usuário da Microsoft para localizar, acessar e consultar elementos de automação da interface do usuário.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)<br/>                         | Expõe métodos que permitem que aplicativos cliente de automação da interface do usuário descubram, acessem e filtrem elementos de automação da interface do usuário. A automação da interface do usuário expõe todos os elementos da automação da interface do usuário como um objeto representado pela interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) . Os membros dessa interface não são específicos de um determinado elemento.<br/> |
| [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2)<br/>                       | Estende a interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) para expor métodos adicionais para controlar a funcionalidade de automação da interface do usuário.<br/>                                                                                                                                                                                                   |
| [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3)<br/>                       | Estende a interface [**IUIAutomation2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation2) para expor métodos adicionais para controlar a funcionalidade de automação da interface do usuário.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4)<br/>                       | Estende a interface [**IUIAutomation3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation3) para expor métodos adicionais para controlar a funcionalidade de automação da interface do usuário.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5)<br/>                       | Estende a interface [**IUIAutomation4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation4) para expor métodos adicionais para controlar a funcionalidade de automação da interface do usuário.<br/>                                                                                                                                                                                                 |
| [**IUIAutomation6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation6)<br/>                       | Estende a interface [**IUIAutomation5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation5) para expor métodos adicionais para controlar a funcionalidade de automação da interface do usuário.<br/>                                                                                                                                                                                                 |
| [**IUIAutomationCacheRequest**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationcacherequest)<br/> | Expõe propriedades e métodos de uma solicitação de cache. Os aplicativos cliente usam essa interface para especificar as propriedades e os padrões de controle a serem armazenados em cache quando um elemento de automação da interface do usuário é obtido.<br/>                                                                                                                                                 |
| [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)<br/>           | Expõe métodos e propriedades para um elemento de automação de interface do usuário, que representa um item de interface do usuário. <br/>                                                                                                                                                                                                                                                        |
| [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2)<br/>         | Estende a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . <br/>                                                                                                                                                                                                                                                             |
| [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3)<br/>         | Estende a interface [**IUIAutomationElement2**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4)<br/>         | Estende a interface [**IUIAutomationElement3**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement3) . <br/>                                                                                                                                                                                                                                                           |
| [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5)<br/>         | Estende a interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) para fornecer acesso a dados de ponto de referência atuais e armazenados em cache.<br/>                                                                                                                                                                                                      |
| [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6)<br/>         | Estende a interface [**IUIAutomationElement5**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement5) para fornecer acesso às descrições completas atuais e armazenadas em cache.<br/>                                                                                                                                                                                                  |
| [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7)<br/>         | Estende a interface [**IUIAutomationElement6**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement6) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8)<br/>         | Estende a interface [**IUIAutomationElement7**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement7) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElement9**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement9)<br/>         | Estende a interface [**IUIAutomationElement8**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement8) .<br/>                                                                                                                                                                                                                                                            |
| [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray)<br/> | Representa uma coleção de elementos de automação da interface do usuário.<br/>                                                                                                                                                                                                                                                                                              |
| [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar)<br/>       | Expõe métodos para registrar novos padrões de controle, propriedades e eventos.<br/>                                                                                                                                                                                                                                                                   |
| [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)<br/>     | Expõe as propriedades e os métodos que os aplicativos cliente de automação da interface do usuário usam para exibir e navegar pelos elementos de automação da interface do usuário na área de trabalho. <br/>                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de automação da interface do usuário](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





