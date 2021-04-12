---
title: Acessibilidade de controle ActiveX sem janela
description: Esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles ActiveX sem janela do Microsoft estejam acessíveis.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366403"
---
# <a name="windowless-activex-control-accessibility"></a>Acessibilidade de controle ActiveX sem janela

Esta seção descreve como usar a API de acessibilidade do Windows para garantir que os controles ActiveX sem janela do Microsoft estejam acessíveis.

O Windows 8 inclui novas interfaces de API de acessibilidade do Windows que simplificam a tarefa de implementar a acessibilidade para controles ActiveX sem janela. A API inclui interfaces que são implementadas em um controle sem janela e no contêiner de controle, permitindo que o controle sem janela e seu contêiner funcionem juntos para fornecer informações de acessibilidade sobre o controle sem janela. A API dá suporte aos seguintes cenários:

-   Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.
-   Controles do Microsoft Acessibilidade Ativa sem janela hospedados em um contêiner de controle de automação da interface do usuário da Microsoft.
-   Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle do Microsoft Acessibilidade Ativa.
-   Controles sem janela de automação da interface do usuário hospedados em um contêiner de controle de automação de interface

A tabela a seguir lista as interfaces que dão suporte a controles ActiveX sem janelas e identifica os objetos que implementam as interfaces.



| Objeto              | MSAA                                                                             | Automação de Interface de Usuário                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Objeto de controle      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Site de controle        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Raiz da janela do host | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Nesta seção

-   [Como usar a automação da interface do usuário para tornar um controle ActiveX sem janela acessível](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Como usar a MSAA para tornar um controle ActiveX sem janela acessível](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Como hospedar um controle ActiveX sem janela de automação da interface do usuário](host-a-ui-automation-windowless-activex-control.md)
-   [Como hospedar um controle ActiveX sem janela do MSAA](host-an-msaa-windowless-activex-control.md)

 

 