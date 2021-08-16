---
description: Descreve a introdução de bibliotecas para Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows Bibliotecas de shell no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f120f1bc4e4208a7e6bbf35bbcfc4717ed05dfb7344658a80b1ea1d9a3ba50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969595"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows Bibliotecas de shell no Windows

Este tópico descreve a introdução de bibliotecas para Windows 7 e posteriores. Bibliotecas são um recurso Windows Shell. Para acessar Windows shell, como bibliotecas, os desenvolvedores de terceiros dos aplicativos Windows Search devem primeiro implementar um armazenamento de dados do Shell. Para obter mais informações, [consulte Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Este tópico é organizado da seguinte forma:

- [Bibliotecas](#libraries)
  - [Pontos de entrada de dados do usuário](#user-data-entry-points)
  - [Coleções de pastas](#collections-of-folders)
  - [Pastas com suporte em bibliotecas](#supported-folders-in-libraries)
  - [Armazenamento com suporte](#storage-backed)
  - [Contêineres do Shell do Sistema de Arquivos não](#non-file-system-shell-containers)
  - [Descrições da biblioteca](#library-descriptions)
- [Tópicos relacionados](#related-topics)

## <a name="libraries"></a>Bibliotecas

No Windows 7 e posteriores, as bibliotecas são o repositório padrão de dados do usuário. Os usuários podem procurar seus arquivos da mesma maneira que em uma pasta ou podem exibir seus arquivos organizados por propriedades como data, tipo e autor. Ao contrário de uma pasta, uma biblioteca não armazena itens, mas exibe arquivos armazenados em várias pastas ao mesmo tempo. As bibliotecas fornecem um único ponto de acesso e dinâmicas de exibição rica para os usuários de seu conteúdo agregado. Por exemplo, se um usuário tiver arquivos de música em pastas em uma unidade externa, além da pasta **Minha** Música, ele poderá acessar imediatamente todos os arquivos de música por meio da biblioteca De música.

### <a name="user-data-entry-points"></a>Pontos de entrada de dados do usuário

Bibliotecas padrão (como **Meus Documentos**, **Minhas Imagens** e assim por diante) são equivalentes à [Pasta Conhecida](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). As bibliotecas padrão fornecem pontos de entrada familiares para os usuários, mas como o conteúdo da biblioteca não está limitado às bibliotecas de conteúdo da Pasta Conhecida, os usuários têm mais liberdade para determinar onde os documentos e a mídia devem ser armazenados. As bibliotecas são expostas por meio do namespace do Shell (fonte de dados do Shell). Seu aplicativo pode fornecer aos usuários os mesmos pontos de entrada conhecidos para seus dados habilitando o reconhecimento de biblioteca e a navegação.

### <a name="collections-of-folders"></a>Coleções de pastas

As bibliotecas são coleções de conteúdo definidas pelo usuário. Windows Pesquise as pastas com suporte quando elas são incluídas em bibliotecas. Isso permite a pesquisa instantânea e exibições de disposição de pilha baseada em propriedade em bibliotecas.

### <a name="supported-folders-in-libraries"></a>Pastas com suporte em bibliotecas

Para que as pastas sejam suportadas em bibliotecas, elas devem ser indexadas no computador local e indexadas em um computador Windows remoto ou indexadas em um servidor com arquivos indexados pelo Windows Search.

As pastas sem suporte são impedidas de serem adicionadas por usuários na caixa Windows de gerenciamento de biblioteca. Se pastas remotas não indexadas são adicionadas a uma biblioteca usando a API [IShellLibrary,](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) a experiência do usuário da biblioteca será revertida para a biblioteca **Cofre Modo**. No **Cofre modo,** como exibições de disposição de pilha baseada em propriedade, sugestões de filtro e suporte à pesquisa **do Menu** Iniciar são removidos da biblioteca afetada.

A tabela a seguir lista as pastas incluídas em bibliotecas usando a caixa de diálogo de gerenciamento de biblioteca do Windows Explorer e pastas sem suporte no **modo Cofre :**

| Pastas com suporte                                                                                                                            | Pastas sem suporte                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Discos rígidos NTFS e FAT32 fixos e externos                                                                                                | Unidades removíveis (como pendrives e cartões SD)                                                     |
| Compartilhamentos indexados pelo Windows Search (como servidores departamentos e em computadores que executam Windows 10 e Windows 7 Home Edition) | Mídia removível (como CDs e DVDs)                                                                  |
| Compartilhamentos que estão disponíveis offline (como **Redirecionado Meus Documentos**, **Cache do Lado do Cliente**)                                               | Compartilhamentos de rede que não estão disponíveis offline nem indexados remotamente (como unidades NAS)             |
| n/d                                                                                                                                          | Outras fontes de dados (como Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive e assim por diante) |

### <a name="storage-backed"></a>Storage-Backed

Bibliotecas são coleções de pastas de armazenamento. Os usuários podem salvar e copiar arquivos diretamente em uma biblioteca, pois cada biblioteca tem um local de salvar padrão para o que enviar esses arquivos. Para bibliotecas padrão, essa é a Pasta Conhecida do usuário incluída em uma biblioteca (como **Meus Documentos**) ou a primeira pasta adicionada a uma biblioteca personalizada. Essa é a pasta em que os arquivos vão quando um usuário arrasta e solta arquivos em uma biblioteca ou salva em uma biblioteca com a caixa de diálogo de arquivo comum. O usuário pode alterar o local de salvar padrão de uma biblioteca a qualquer momento, mas se remover o local de salvar padrão, a próxima pasta na biblioteca será selecionada como o novo local de salvar. Os usuários também podem salvar em qualquer pasta em que tenham permissões que foram incluídas em uma biblioteca.

### <a name="non-file-system-shell-containers"></a>Contêineres do Shell do Sistema de Arquivos não

As bibliotecas podem conter contêineres do Shell do sistema de arquivos, como **Computer** **e Painel de Controle**, mas contêm itens do sistema de arquivos. As pastas e o conteúdo da biblioteca podem ser enumerados e acessados usando APIs para arquivos e pastas do sistema de arquivos em sistemas operacionais anteriores. Se seu aplicativo depender muito de APIs específicas do sistema de arquivos, a API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) poderá ser usada para obter os caminhos do sistema de arquivos de pastas e arquivos em bibliotecas. Na maioria dos casos, é recomendável usar o modelo de programação shell para dar suporte a várias versões Windows e flexibilidade de item. Para obter mais informações, [consulte Navegando no namespace do Shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descrições da biblioteca

As descrições da biblioteca são salvas no disco como um arquivo XML na pasta %appdata%Microsoft Windows Libraries (e, potencialmente, como \\ \\ **Bibliotecas FOLDERID). \_** Para obter mais informações sobre **\_ bibliotecas FOLDERID,** consulte [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Os arquivos de descrição da biblioteca são arquivos XML com a extensão de nome de arquivo .library-ms. Os arquivos nunca devem ser acessados ou editados por aplicativos. O texto do caminho da pasta persistido nos arquivos de descrição da biblioteca nem sempre é atual. As pastas de biblioteca são persistentes no arquivo de descrição da biblioteca no formato de Links do [Shell](/windows/desktop/shell/links) binário serializado. Para obter mais informações sobre bibliotecas e o esquema de Descrição da Biblioteca, consulte [Esquema de Descrição da Biblioteca](../shell/library-schema-entry.md). Para obter mais informações sobre conectores de pesquisa federadas e o esquema Descrição do Conector de Pesquisa, Esquema [de Descrição do Conector de Pesquisa](search-sconn-desc-schema-entry.md).

> [OBSERVAÇÃO]  
> Os aplicativos sempre devem usar o modelo de programação shell ou a API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para consumir e manipular o conteúdo da biblioteca e nunca tentar acessar ou editar manualmente o arquivo de descrição da biblioteca.

## <a name="related-topics"></a>Tópicos relacionados

[Windows 7 Search](./-search-3x-wds-overview.md)

[Novidades da Windows 7 Search](new-for-windows-7-search.md)

[Indexando eventos de priorização e de conjuntos de linhas Windows 7](indexing-prioritization-and-rowset-events.md)