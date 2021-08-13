---
title: Acessibilidade de controle ActiveX janela
description: Esta seção descreve como usar o Windows API de Acessibilidade para garantir que os controles microsoft ActiveX sem janelas sejam acessíveis.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563451"
---
# <a name="windowless-activex-control-accessibility"></a>Acessibilidade de controle ActiveX janela

Esta seção descreve como usar o Windows API de Acessibilidade para garantir que os controles microsoft ActiveX sem janelas sejam acessíveis.

Windows 8 inclui novas interfaces Windows API de Acessibilidade que simplificam a tarefa de implementar a acessibilidade para controles ActiveX janela. A API inclui interfaces implementadas em um controle sem janela e no contêiner de controle, permitindo que o controle sem janelas e seu contêiner trabalhem juntos para fornecer informações de acessibilidade sobre o controle sem janela. A API dá suporte aos seguintes cenários:

-   Microsoft Active Accessibility controles sem janela hospedados em um contêiner de Microsoft Active Accessibility controle.
-   Microsoft Active Accessibility sem janela hospedados em um contêiner de controle Automação da Interface do Usuário Microsoft.
-   Automação da Interface do Usuário sem janela hospedados em um contêiner Microsoft Active Accessibility controle.
-   Automação da Interface do Usuário controles sem janela hospedados em um contêiner Automação da Interface do Usuário controle.

A tabela a seguir lista as interfaces que suportam controles sem janela ActiveX e identifica os objetos que implementam as interfaces.



| Objeto              | Msaa                                                                             | Automação de Interface de Usuário                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objeto de controle      | [**Iaccessiblehandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Site de controle        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Raiz da janela do host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Nesta seção

-   [Como usar o Automação da Interface do Usuário tornar um controle de ActiveX sem janelas acessível](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Como usar a MSAA para tornar um controle de ActiveX sem janelas acessível](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Como hospedar um controle Automação da Interface do Usuário sem ActiveX janela](host-a-ui-automation-windowless-activex-control.md)
-   [Como hospedar um controle de ActiveX MSAA](host-an-msaa-windowless-activex-control.md)

 

 