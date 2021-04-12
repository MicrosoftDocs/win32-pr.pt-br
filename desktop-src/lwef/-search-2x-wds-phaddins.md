---
title: Desenvolvendo suplementos de manipulador de protocolo
description: Você pode estender o Microsoft Windows Desktop Search (WDS) para incluir novos armazenamentos de dados implementando um manipulador de protocolo personalizado.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a8688621f7d2fda653d769c0e1dfdadd240f49
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499044"
---
# <a name="developing-protocol-handler-add-ins"></a>Desenvolvendo suplementos de manipulador de protocolo

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Você pode estender o Microsoft Windows Desktop Search (WDS) para incluir novos armazenamentos de dados implementando um manipulador de protocolo personalizado.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexando armazenamentos de dados com manipuladores de protocolo

Um repositório de dados é uma fonte de conteúdo (um sistema de banco de dado, um diretório, um sistema de arquivos) em que os dados são armazenados e podem ser rastreados pelo indexador do WDS. O repositório pode ser hierárquico (como um banco de dados) ou baseado em link (como um site). Um manipulador de protocolo permite que aplicativos de indexação como o WDS rastreiem sistematicamente os nós de um armazenamento de dados para extrair informações relevantes a serem incluídas no índice. Cada manipulador de protocolo é usado para indexar um tipo específico de armazenamento de dados. O WDS é fornecido com manipuladores de protocolo para armazenamentos do sistema de arquivos e para armazenamentos de dados do Microsoft Outlook e do Microsoft Outlook Express (armazenamentos de emails,. Arquivos PST e assim por diante). Ao indexar emails do Outlook, por exemplo, o manipulador de protocolo rastreia todas as mensagens em todas as pastas que extraem informações de cada mensagem e anexo. Essas informações são passadas para o indexador para incluir no catálogo do WDS.

Muitas vezes, os usuários precisam pesquisar outros armazenamentos de dados, como bancos de dados herdados, armazenamentos de email ou estruturas de data sem suporte pelo WDS. Você pode estender o WDS para rastrear um novo armazenamento de dados usando ou implementando um manipulador de protocolo especificamente para esse armazenamento de dados. Primeiro, primeiro você deve determinar se um manipulador de protocolo já existe para seu armazenamento de dados, talvez para uso com outro aplicativo, como os serviços do SharePoint. Nesse caso, você pode instalar esse manipulador de protocolo no sistema. No entanto, se outro manipulador de protocolo não existir, você precisará implementar um. Os manipuladores de protocolo do WDS usam as mesmas especificações de design que os serviços do SharePoint e, em geral, podem ser usados de maneira intercambiável.

Além disso, se o armazenamento de dados contiver dados ou tipos de arquivos diferentes de um dos tipos de arquivo 200 com suporte no WDS, você também precisará implementar um filtro para acessar e indexar o conteúdo dos itens no repositório. O WDS 2. x usa o manipulador de protocolo e a tecnologia [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)usada pelos serviços do SharePoint. Se você já tiver filtros para um repositório e tipo de arquivo específicos instalados no sistema que está sendo indexado, o WDS usará as interfaces existentes para indexar esses dados.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Roteiro para adicionar novos armazenamentos de dados

Para estender o WDS para rastrear novos armazenamentos de dados, você pode criar um manipulador de protocolo e um ou mais dos seguintes suplementos: manipulador de menu de contexto, manipulador de ícone e um suplemento SearchProtocolOptions.

1.  Criar e registrar um manipulador de protocolo multithread para o armazenamento de dados:
    -   **ISearchProtocol** -essa interface acessa um protocolo e MAPEIA uma URL para um IUrlAccessor.
    -   **IUrlAccessor** -essa é a interface principal usada para acessar itens da fonte de conteúdo e ligar o conteúdo ao filtro apropriado.
    -   **IProtocolHandlerSite** -essa interface é usada para solicitar e carregar filtros adicionais.
    -   **IFilter** – essa interface retorna a URL de cada item em uma pasta como propriedades de valor para processamento.

    > [!Note]
    >
    > A funcionalidade de suplemento mínima necessária para retornar os resultados da pesquisa de um armazenamento de dados não hierárquico é uma implementação das interfaces ISearchProtocol e IUrlAccessor.

     

2.  Implemente a interface ISearchProtocolOptions para incluir opções de manipulador de protocolo personalizadas, como páginas de início predefinidas:
    -   **ISearchProtocolOptions** -essa interface define as URLs padrão para o manipulador de protocolo para processar, determina quais são os requisitos para um manipulador de protocolo e determina se os requisitos foram atendidos em determinado sistema.
3.  Estenda o Shell para incluir elementos da interface do usuário, como menus de contexto e ícones específicos de arquivo, implementando as seguintes interfaces:
    -   **IShellFolder** -essa interface, que é usada para gerenciar pastas, é necessária para fornecer as interfaces IContextMenu e IExtractIcon para uma URL em um novo repositório.
    -   **IPersistFolder** -essa interface é necessária para instruir um objeto de pasta do Shell a se inicializar.
    -   **IPersist** -essa interface fornece o identificador de classe (CLSID) de um objeto que pode ser armazenado de forma persistente no sistema.
    -   **IContextMenu** -essa interface define o menu de contexto de clique com o botão direito do mouse para um item apontado por URL.
    -   **IExtractIcon** -essa interface define o ícone a ser exibido para um item apontado por URL.
4.  Implemente um mecanismo para notificar o indexador de alterações no armazenamento de dados:
    -   **ISearchItemsChangedSink** -essa interface permite que o manipulador de protocolo notifique o índice de alterações no armazenamento de dados. Isso melhora o desempenho garantindo que o indexador não rastreie todo o armazenamento em índices incrementais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Implementando um manipulador de protocolo para o WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Adicionando ícones, visualizações e menus de contexto com extensões de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notificando o índice das alterações](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Instalando e Registrando manipuladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 