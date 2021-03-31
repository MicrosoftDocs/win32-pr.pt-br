---
title: Como hospedar um controle ActiveX sem janela do MSAA
description: Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam o Microsoft Acessibilidade Ativa.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, controle ActiveX sem janela
- Controle ActiveX sem janela, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641155"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Como hospedar um controle ActiveX sem janela do MSAA

Saiba como criar um contêiner de controle que pode hospedar controles Microsoft ActiveX sem janelas que implementam o Microsoft Acessibilidade Ativa. Seguindo as etapas descritas aqui, você pode garantir que todos os controles sem janela baseados no Microsoft Acessibilidade Ativa hospedados no seu contêiner de controle estejam acessíveis para aplicativos cliente de tecnologia assistencial (AT).

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles ActiveX](/windows/desktop/com/activex-controls)
-   [Acessibilidade Ativa da Microsoft](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação do COM (Microsoft Win32 e Component Object Model)
-   Controles ActiveX sem janela
-   Servidores Microsoft Acessibilidade Ativa

## <a name="instructions"></a>Instruções

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Etapa 1: fornecer a interface IAccessible raiz em nome do controle sem janela.

Sempre que o sistema precisar do ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para a raiz de um controle sem janela, o sistema consultará o contêiner de controle. Para recuperar o ponteiro, o contêiner chama a implementação de controle sem janela do método [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) .

Se o contêiner de controle tiver uma implementação de Acessibilidade Ativa da Microsoft, ele poderá retornar o ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do controle sem janela para o sistema.

Se o contêiner de controle tiver uma implementação de automação de interface do usuário da Microsoft, chame a função [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) para obter um ponteiro de interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que represente o controle e, em seguida, retorne o ponteiro de interface **IRawElementProviderSimple** para o sistema.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Etapa 2: responder à mensagem do WM \_ GetObject em nome do controle sem janela.

Quando um aplicativo cliente responde a um WinEvent gerado por um controle sem janela, o contêiner de controle recebe uma mensagem do [**WM \_ GetObject**](wm-getobject.md) em nome do controle. A mensagem inclui a ID de objeto do controle sem janela que disparou o evento.

O contêiner de controle responde pesquisando o controle sem janela que "possui" a ID de objeto e, em seguida, chamando o método [**IAccessibleHandler:: AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) do controle. O método **AccessibleObjectFromID** retorna o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o item da interface do usuário, e o contêiner de controle retorna o ponteiro para o sistema, que o encaminha para o aplicativo cliente.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Etapa 3: implementar a interface IAccessibleWindowlessSite.

1.  Implemente o método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) .

    Quando um aplicativo cliente precisa de informações de acessibilidade sobre o pai do provedor raiz do controle sem janela, o sistema chama o método [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) do controle sem janela. O controle responde chamando o método [**IAccessibleWindowlessSite:: GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) do contêiner de controle, que fornece o ponteiro [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do pai do controle sem janela.

2.  Implemente os métodos [**IAccessibleWindowlessSite:: AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)e [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    Seu contêiner de controle deve manter um mapeamento de intervalos de ID de objeto para controles sem janela. O mapeamento permite que o contêiner de controle identifique o controle que deve responder a uma solicitação específica para uma ID de objeto. A tabela a seguir mostra um exemplo de mapeamento de intervalos de ID de objeto para controles sem janela.

    

    | Base do intervalo | Tamanho do intervalo | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Controle 1 |
    | 1500       | 1000       | Controle 2 |
    | 2500       | 2000       | Controle 1 |

    

     

    O contêiner de controle deve manter o mapeamento de intervalos de ID de objeto para controles sem janelas para si mesmo e todos os filhos sem janelas. Os intervalos de ID de objeto não precisam ser adjacentes uns aos outros. Além disso, para evitar ataques de negação de serviço, o contêiner de controle pode colocar limites no número de intervalos que são concedidos a um controle específico. No entanto, é útil permitir mais de um intervalo por controle, para permitir que um controle cresça.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Etapa 4: opcional: implementar a interface IAccessibleHostingElementProviders.

Implemente a interface [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) se o seu contêiner de controle tiver uma implementação do Microsoft acessibilidade ativa Server e o servidor for a raiz de uma árvore de acessibilidade que inclui controles ActiveX sem janela que dão suporte à automação da interface do usuário. A interface **IAccessibleHostingElementProviders** tem um único método, [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), que recupera os ponteiros de interface [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) de todos os controles ActiveX sem janela de automação da interface do usuário hospedados pelo seu contêiner de controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como hospedar um controle ActiveX sem janela de automação da interface do usuário](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Acessibilidade de controle ActiveX sem janela](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 