---
title: Desenvolvendo complementos do manipulador de protocolo
description: Você pode estender o Microsoft Windows WDS (Desktop Search) para incluir novos armazenamentos de dados implementando um manipulador de protocolo personalizado.
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726496"
---
# <a name="developing-protocol-handler-add-ins"></a>Desenvolvendo complementos do manipulador de protocolo

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

Você pode estender o Microsoft Windows WDS (Desktop Search) para incluir novos armazenamentos de dados implementando um manipulador de protocolo personalizado.

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indexando armazenamentos de dados com manipuladores de protocolo

Um armazenamento de dados é uma fonte de conteúdo (um sistema de banco de dados, um diretório, um sistema de arquivos) em que os dados são armazenados e podem ser rastreados pelo Indexador do WDS. O armazenamento pode ser hierárquico (como um banco de dados) ou baseado em link (como um site). Um manipulador de protocolo permite indexar aplicativos como o WDS para rastrear sistematicamente os nós de um armazenamento de dados para extrair informações relevantes a incluir no índice. Cada manipulador de protocolo é usado para indexar um tipo específico de armazenamento de dados. O WDS é enviado com manipuladores de protocolo para armazenamentos de sistema de arquivos e para armazenamentos de dados do Microsoft Outlook e do Microsoft Outlook Express (armazenamentos de email, . Arquivos PST e assim por diante). Ao indexar Outlook email, por exemplo, o manipulador de protocolo rastrea todas as mensagens em todas as pastas que extraem informações de cada mensagem e anexo. Essas informações são passadas para o Indexador a ser incluído no catálogo do WDS.

Geralmente, os usuários precisam pesquisar outros armazenamentos de dados, como bancos de dados herdados, armazenamentos de email ou estruturas de dados sem suporte do WDS. Você pode estender o WDS para rastrear um novo armazenamento de dados usando ou implementando um manipulador de protocolo especificamente para esse armazenamento de dados. Primeiro, você deve primeiro determinar se um manipulador de protocolo já existe para o armazenamento de dados, talvez para uso com outro aplicativo, como SharePoint Services. Nesse caso, você pode instalar esse manipulador de protocolo no sistema. Se, no entanto, outro manipulador de protocolo não existir, você precisará implementar um. Os manipuladores de protocolo WDS usam as mesmas especificações de design SharePoint Services e geralmente podem ser usados de forma intercambiável.

Além disso, se o armazenamento de dados contiver dados ou tipos de arquivo diferentes de um dos 200 tipos de arquivos com suporte do WDS, você também precisará implementar um filtro para acessar e indexar o conteúdo dos itens no armazenamento. O WDS 2.x usa o manipulador de protocolo e a [**tecnologia IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)usada pelo SharePoint Services. Se você já tiver filtros para um tipo de arquivo e armazenamento específicos instalados no sistema que está sendo indexado, o WDS usará as interfaces existentes para indexar esses dados.

 

## <a name="roadmap-to-adding-new-data-stores"></a>Roteiro para adicionar novos armazenamentos de dados

Para estender o WDS para rastrear novos armazenamentos de dados, você pode criar um manipulador de protocolo e um ou mais dos seguintes complementos: manipulador de menu de contexto, manipulador de ícones e um complemento SearchProtocolOptions.

1.  Crie e registre um manipulador de protocolo multithread para o armazenamento de dados:
    -   **ISearchProtocol** – essa interface acessa um protocolo e mapeia uma URL para um IUrlAccessor.
    -   **IUrlAccessor** – essa é a interface principal usada para acessar itens da fonte de conteúdo e vincular o conteúdo ao filtro apropriado.
    -   **IProtocolHandlerSite** – essa interface é usada para solicitar e carregar filtros adicionais.
    -   **IFilter** – essa interface retorna a URL de cada item em uma pasta como propriedades de valor para processamento.

    > [!Note]
    >
    > A funcionalidade de complemento mínima necessária para retornar os resultados da pesquisa de um armazenamento de dados não hierárquico é uma implementação de interfaces ISearchProtocol e IUrlAccessor.

     

2.  Implemente a interface ISearchProtocolOptions para incluir opções de manipulador de protocolo personalizadas, como páginas de início predefinidos:
    -   **ISearchProtocolOptions** – essa interface define as URLs padrão para o manipulador de protocolo processar, determina quais são os requisitos para um manipulador de protocolo e determina se os requisitos foram atendidos em um determinado sistema.
3.  Estenda o Shell para incluir elementos de interface do usuário, como menus de contexto e ícones específicos do arquivo, implementando as seguintes interfaces:
    -   **IShellFolder** – essa interface, que é usada para gerenciar pastas, é necessária para fornecer as interfaces IContextMenu e IExtractIcon para uma URL em um novo armazenamento.
    -   **IPersistFolder** – essa interface é necessária para instruir um objeto de pasta shell a se inicializar.
    -   **IPersist** – essa interface fornece o CLSID (identificador de classe) de um objeto que pode ser armazenado persistentemente no sistema.
    -   **IContextMenu** – essa interface define o menu de contexto de clique com o botão direito do mouse para um item apontado pela URL.
    -   **IExtractIcon** – essa interface define o ícone a ser exibido para um item apontado pela URL.
4.  Implemente um mecanismo para notificar o Indexador sobre as alterações no armazenamento de dados:
    -   **ISearchItemsChangedSink** – essa interface permite que o manipulador de protocolo notifique o Índice de alterações no armazenamento de dados. Isso melhora o desempenho, garantindo que o Indexador não rastrea todo o armazenamento em índices incrementais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Implementando um manipulador de protocolo para WDS](-search-2x-wds-phimplementing.md)
</dt> <dt>

[Adicionando ícones, visualizações e menus de contexto com extensões do Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Notificando o índice de alterações](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Instalando e registrando manipuladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 