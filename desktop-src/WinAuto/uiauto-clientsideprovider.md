---
title: Implementando um provedor de automação de interface do usuário de Client-Side (proxy)
description: Este tópico descreve como gravar um provedor de proxy para um controle sem suporte e adicioná-lo à lista de proxies usados por aplicativos cliente.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Automação da interface do usuário, implementação do provedor do lado do cliente
- Automação da interface do usuário, implementação do provedor
- Automação da interface do usuário, Implementando provedores do lado do cliente
- Automação da interface do usuário, Implementando provedores
- Automação da interface do usuário, proxies
- proxies
- provedores do lado do cliente
- provedores, implementando
- Implementando provedores do lado do cliente
- Implementando provedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2bdb4a94ba6e693792508de5c573317299b0d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007636"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementando um provedor de automação de interface do usuário de Client-Side (proxy)

A automação da interface do usuário da Microsoft fornece um conjunto de proxies para a maioria dos controles padrão, como os usados nos aplicativos Microsoft Win32, Windows Forms e Windows Presentation Foundation (WPF). No entanto, muitos controles personalizados e controles de terceiros não implementam provedores nativos de automação da interface do usuário. Para ser acessível a aplicativos cliente de automação da interface do usuário, esses controles devem ser fornecidos com provedores do lado do cliente, também conhecidos como *provedores de proxy* ou *proxies*.

Este tópico descreve como gravar um provedor de proxy para um controle sem suporte e adicioná-lo à lista de proxies usados por aplicativos cliente. Ele contém os seguintes tópicos:

-   [O que é um proxy?](#what-is-a-proxy)
-   [O que é uma fábrica de proxy?](#what-is-a-proxy-factory)
-   [Mapeamento de fábrica de proxy](#proxy-factory-mapping)
-   [Gerenciando proxies padrão](#managing-default-proxies)
-   [Tópicos relacionados](#related-topics)

Para obter exemplos de código que mostram como implementar provedores de proxy, consulte os [Tópicos de instruções para provedores de automação da interface do usuário](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>O que é um proxy?

Um provedor do lado do cliente, ou proxy, é um objeto que implementa a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) em nome de um controle que não tem uma implementação de **IRawElementProviderSimple** própria. Sem um proxy, esse controle é amplamente opaco para a automação da interface do usuário, que pode fornecer apenas informações básicas disponíveis no identificador de janela (**HWND**), como o local do controle.

## <a name="what-is-a-proxy-factory"></a>O que é uma fábrica de proxy?

Cada proxy requer uma *fábrica de proxy* correspondente, que é um objeto que expõe a interface [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) . A automação da interface do usuário mantém uma tabela interna de *entradas de fábrica de proxy*, cada uma delas contendo uma referência à fábrica de proxy para cada proxy e um conjunto de condições. Quando a automação da interface do usuário encontra um controle que não tem uma implementação [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) nativa, ele procura uma entrada de fábrica de proxy cujas condições indicam que ele dá suporte ao controle. A automação da interface do usuário pesquisa a tabela desde o início e, quando encontra uma entrada correspondente, a automação da interface do usuário chama o método [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) da fábrica. Se o proxy correspondente for criado com êxito, a automação da interface do usuário interromperá a pesquisa e usará o objeto proxy recém-criado; caso contrário, a automação da interface do usuário continuará pesquisando.

Um aplicativo cliente cria uma instância de uma entrada de fábrica de proxy usando o método [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) , que retorna um ponteiro de interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Os clientes usam métodos expostos por **IUIAutomationProxyFactoryEntry** para especificar o conjunto de condições que a fábrica de proxy usa para criar o proxy.

Quando chama [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider), a automação da interface do usuário passa parâmetros que o objeto de fábrica de proxy pode usar para determinar se o proxy dá suporte adequado ao controle personalizado. Nesse caso, a fábrica de proxy cria uma instância do proxy e retorna o ponteiro de interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ; caso contrário, ele retorna um ponteiro **nulo** .

## <a name="proxy-factory-mapping"></a>Mapeamento de fábrica de proxy

Por padrão, a automação da interface do usuário pesquisa a tabela de fábrica de proxy na seguinte ordem.



| Ordem | Proxy                        | Descrição                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: proxy sem controle | Para Windows com o nome de classe exato ou o nome de classe base "ComboBoxEx32".         |
| 2     | Microsoft: proxy sem controle | Para Windows com o nome de classe exato ou o nome de classe base "WorkerW".              |
| 3     | Microsoft: proxy sem controle | Para Windows com o nome de classe exato ou o nome de classe base "SHELLDLL \_ DefView".    |
| 4     | Microsoft: proxy de contêiner   | Para Windows com o nome exato da classe ou o nome da classe base " \# 32770".              |
| 5     | Microsoft: proxy de contêiner   | Para Windows com um nome de classe ou nome de classe base que contém "AfxControlBar".     |
| 6     | Microsoft: proxy de TreeView    | Para Windows com um nome de classe ou nome de classe base que contém "SysTreeView32".     |
| 7     | Microsoft: proxy de ListView    | Para Windows com um nome de classe ou nome de classe base que contém "SysListView32" (1). |
| 8     | Microsoft: proxy de ListView    | Para Windows com um nome de classe ou nome de classe base que contém "SysListView32" (2). |
| 9     | Microsoft: proxy MSAA        | Para qualquer janela.                                                                  |



 

Os proxies 7 e 8 são entradas duplicadas para o controle SysListView32. Sem modificação, o proxy 7 sempre é usado para o controle SysListView32 e o proxy 8 nunca é usado. O proxy 8 é usado somente para itens de lista visíveis e normalmente é usado por aplicativos cliente que funcionam apenas com elementos visíveis ou que têm requisitos de desempenho estritos. Esses clientes podem remover o proxy 7.

O proxy 9, o Microsoft Acessibilidade Ativa ao proxy de automação da interface do usuário, sempre deve ser a última entrada na tabela. Isso permite que a funcionalidade de fallback do Microsoft Acessibilidade Ativa para controles que implementam o Microsoft Acessibilidade Ativa, mas não a automação da interface do usuário.

Ao modificar entradas na tabela de fábrica de proxy, você deve avaliar cuidadosamente a nova posição das entradas. Recomendamos que as entradas para proxies personalizados sejam colocadas após os proxies de não controle e de contêiner, mas antes do Microsoft Acessibilidade Ativa ao proxy de automação da interface do usuário. Além disso, embora seja possível que o código na chamada para [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) determine se ele deve dar suporte a um determinado identificador de janela (**HWND**), é mais eficiente permitir que a automação da interface do usuário selecione o proxy com base no nome da classe e mantenha o código condicional no método **CreateProvider** para um mínimo.

A automação da interface do usuário mantém uma tabela de fábrica de proxy separada para cada cliente. Quando um cliente altera sua tabela de proxy, as alterações afetam somente o próprio cliente; outros clientes não são afetados.

## <a name="managing-default-proxies"></a>Gerenciando proxies padrão

Quando um aplicativo cliente cria o objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , a tabela de fábrica de proxy inicialmente contém entradas somente para os provedores de proxy padrão para controles padrão. Usando a interface [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , os clientes podem adicionar novas entradas, remover entradas indesejadas, alterar a ordem das entradas e assim por diante. Um cliente pode recuperar um ponteiro de interface **IUIAutomationProxyFactoryMapping** chamando o método [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) .

A tabela de proxies disponíveis contém uma interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para cada proxy. Cada **IUIAutomationProxyFactoryEntry** especifica o [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) e a classe de controle que o proxy atende e define como os eventos devem ser manipulados.

A tabela de proxies é representada por uma interface [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , que pode ser obtida na propriedade [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) . Um aplicativo pode usar métodos **IUIAutomationProxyFactoryMapping** para adicionar e excluir proxies. Para criar uma nova entrada a ser adicionada a essa tabela, use [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) para obter a interface e, em seguida, use os métodos [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) para definir a classe de controle aplicável e o comportamento do proxy.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar um provedor de automação de interface do usuário Client-Side (proxy)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Guia do programador do provedor de automação de interface do usuário](uiauto-providerportal.md)
</dt> </dl>

 

 