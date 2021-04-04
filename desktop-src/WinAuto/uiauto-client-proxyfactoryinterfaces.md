---
title: Interfaces de fábrica de proxy para clientes
description: Esta seção descreve as interfaces de fábrica de proxy para aplicativos cliente de automação de interface do usuário não gerenciado.
ms.assetid: 46c6720a-19c2-4ddd-893c-1a46af0642fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc1827ab36a221dcd7f27e5b2a05de91931b0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006014"
---
# <a name="proxy-factory-interfaces-for-clients"></a>Interfaces de fábrica de proxy para clientes

Esta seção descreve as interfaces de fábrica de proxy para aplicativos cliente de automação de interface do usuário não gerenciado.

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                                      | Descrição                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory)<br/>               | Expõe propriedades e métodos de um objeto que cria um provedor de automação de interface do usuário da Microsoft para elementos de interface do usuário que não têm suporte nativo para automação da interface do usuário. Essa interface é implementada por proxies.<br/>                                                                          |
| [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry)<br/>     | Representa uma fábrica de proxy na tabela mantida pela automação da interface do usuário e expõe propriedades e métodos que podem ser usados por aplicativos cliente para interagir com objetos [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) .<br/>                                   |
| [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping)<br/> | Expõe propriedades e métodos para uma tabela de fábricas de proxy. Cada entrada de tabela é representada por uma interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . As entradas estão na ordem em que o sistema tentará usar os proxies.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de automação da interface do usuário](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





