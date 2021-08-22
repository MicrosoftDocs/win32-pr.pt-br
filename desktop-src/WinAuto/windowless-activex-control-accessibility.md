---
title: acessibilidade de controle de ActiveX sem janelas
description: esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles do Microsoft ActiveX sem janelas sejam acessíveis.
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
# <a name="windowless-activex-control-accessibility"></a>acessibilidade de controle de ActiveX sem janelas

esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles do Microsoft ActiveX sem janelas sejam acessíveis.

Windows 8 inclui novas interfaces de API de acessibilidade do Windows que simplificam a tarefa de implementar a acessibilidade para controles de ActiveX sem janelas. A API inclui interfaces que são implementadas em um controle sem janela e no contêiner de controle, permitindo que o controle sem janela e seu contêiner funcionem juntos para fornecer informações de acessibilidade sobre o controle sem janela. A API dá suporte aos seguintes cenários:

-   Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.
-   Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle de automação da interface do usuário da Microsoft.
-   Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.
-   Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle de automação de interface

a tabela a seguir lista as interfaces que dão suporte a controles de ActiveX sem janelas e identifica os objetos que implementam as interfaces.



| Objeto              | MSAA                                                                             | Automação de Interface de Usuário                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objeto de controle      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Site de controle        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Raiz da janela do host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Nesta seção

-   [como usar a automação da interface do usuário para tornar um controle de ActiveX sem janelas acessível](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [como usar a MSAA para tornar um controle de ActiveX sem janelas acessível](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [como hospedar um controle de ActiveX sem janela de automação da interface do usuário](host-a-ui-automation-windowless-activex-control.md)
-   [como hospedar um controle de ActiveX sem janela MSAA](host-an-msaa-windowless-activex-control.md)

 

 