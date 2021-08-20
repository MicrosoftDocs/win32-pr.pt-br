---
title: Como hospedar um controle de ActiveX MSAA
description: Saiba como criar um contêiner de controle que pode hospedar controles microsoft ActiveX sem janela que implementam Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, controle de ActiveX janela
- Controle de ActiveX janela, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115127"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Como hospedar um controle de ActiveX MSAA

Saiba como criar um contêiner de controle que pode hospedar controles microsoft ActiveX sem janela que implementam Microsoft Active Accessibility. Seguindo as etapas descritas aqui, você pode garantir que todos os controles sem janela baseados em Microsoft Active Accessibility que estão hospedados em seu contêiner de controle sejam acessíveis a aplicativos cliente da AT (tecnologia adaptativa).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [ActiveX Controles](/windows/desktop/com/activex-controls)
-   [Acessibilidade Ativa da Microsoft](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação do Microsoft Win32 e Component Object Model (COM)
-   Controles de ActiveX janela
-   Microsoft Active Accessibility servidores

## <a name="instructions"></a>Instruções

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Etapa 1: forneça a interface IAccessible raiz em nome do controle sem janela.

Sempre que o sistema precisar do ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para a raiz de um controle sem janela, o sistema consultará o contêiner de controle. Para recuperar o ponteiro, o contêiner chama a implementação do controle sem janela do [**método IServiceProvider::QueryService.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))

Se o contêiner de controle tiver uma Microsoft Active Accessibility, ele poderá retornar o ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do controle sem janela para o sistema.

Se o contêiner de controle tiver uma implementação do Microsoft Automação da Interface do Usuário, chame a função [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) para obter um ponteiro de interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que representa o controle e retorne o ponteiro da interface **IRawElementProviderSimple** para o sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Etapa 2: Responder à mensagem WM \_ GETOBJECT em nome do controle sem janela.

Quando um aplicativo cliente responde a um WinEvent gerado por um controle sem janela, o contêiner de controle recebe uma mensagem [**WM \_ GETOBJECT**](wm-getobject.md) em nome do controle. A mensagem inclui a ID do objeto do controle sem janela que gerou o evento.

O contêiner de controle responde procurando o controle sem janela que "possui" a ID do objeto e, em seguida, chamando o método [**IAccessibleHandler::AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) desse controle. O **método AccessibleObjectFromID** retorna o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o item de interface do usuário e o contêiner de controle retorna o ponteiro para o sistema, que o encaminha para o aplicativo cliente.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Etapa 3: Implementar a interface IAccessibleWindowlessSite.

1.  Implemente [**o método IAccessibleWindowlessSite::GetParentAccessible.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible)

    Quando um aplicativo cliente precisa de informações de acessibilidade sobre o pai do provedor raiz do controle sem janela, o sistema chama o método [**IAccessible::get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) do controle sem janela. O controle responde chamando o método [**IAccessibleWindowlessSite::GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) do contêiner de controle, que fornece o ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do pai do controle sem janela.

2.  Implemente os [**métodos IAccessibleWindowlessSite::AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)e [**ReleaseObjectIdRange.**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange)

    O contêiner de controle deve manter um mapeamento de intervalos de ID de objeto para controles sem janela. O mapeamento permite que o contêiner de controle identifique o controle que deve responder a uma solicitação específica para uma ID de objeto. A tabela a seguir mostra um exemplo de intervalos de ID de objeto de mapeamento para controles sem janela.

    

    | Base de intervalo | Tamanho do intervalo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Controle 1 |
    | 1500       | 1000       | Controle 2 |
    | 2500       | 2000       | Controle 1 |

    

     

    O contêiner de controle deve manter o mapeamento de intervalos de ID de objeto para controles sem janela para si mesmo e todos os filhos sem janela. Os intervalos de ID de objeto não precisam ser adjacentes entre si. Além disso, para evitar ataques de negação de serviço, o contêiner de controle pode colocar limites no número de intervalos concedidos a um controle específico. No entanto, é útil permitir mais de um intervalo por controle, para permitir que um controle cresça.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Etapa 4: opcional: implementar a interface IAccessibleHostingElementProviders.

Implemente a interface [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) se o contêiner de controle tiver uma implementação de servidor Microsoft Active Accessibility e o servidor for a raiz de uma árvore de acessibilidade que inclui controles ActiveX sem janela que oferecem suporte Automação da Interface do Usuário. A interface **IAccessibleHostingElementProviders** tem um único método, [**GetEmbeddedFragmentRoots,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)que recupera os ponteiros da interface [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) de todos os controles de ActiveX sem janela Automação da Interface do Usuário que são hospedados pelo contêiner de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como hospedar um controle Automação da Interface do Usuário sem ActiveX janela](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Acessibilidade de controle ActiveX janela](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 