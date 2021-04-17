---
description: Descreve a introdução de bibliotecas para o Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Bibliotecas de shell do Windows no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105761836"
---
# <a name="windows-shell-libraries-in-windows"></a>Bibliotecas de shell do Windows no Windows

Este tópico descreve a introdução de bibliotecas para o Windows 7 e versões posteriores. As bibliotecas são um recurso de shell do Windows. Para acessar a funcionalidade do shell do Windows, como bibliotecas, desenvolvedores de terceiros de aplicativos do Windows Search devem primeiro implementar um armazenamento de dados do Shell. Para obter mais informações, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Este tópico é organizado da seguinte maneira:

- [Bibliotecas](#libraries)
  - [Pontos de entrada de dados do usuário](#user-data-entry-points)
  - [Coleções de pastas](#collections-of-folders)
  - [Pastas com suporte em bibliotecas](#supported-folders-in-libraries)
  - [Com backup em armazenamento](#storage-backed)
  - [Contêineres de shell do sistema não arquivo](#non-file-system-shell-containers)
  - [Descrições da biblioteca](#library-descriptions)
- [Tópicos relacionados](#related-topics)

## <a name="libraries"></a>Bibliotecas

No Windows 7 e versões posteriores, as bibliotecas são o repositório padrão de dados do usuário. Os usuários podem procurar seus arquivos da mesma maneira que fariam em uma pasta ou podem exibir seus arquivos organizados por propriedades, como data, tipo e autor. Ao contrário de uma pasta, uma biblioteca não armazena itens de fato, mas exibe os arquivos armazenados em várias pastas ao mesmo tempo. As bibliotecas fornecem um único ponto de acesso e tabelas dinâmicas de exibição rica para os usuários de seu conteúdo agregado. Por exemplo, se um usuário tiver arquivos de música em pastas em uma unidade externa além da pasta **minhas músicas** , eles poderão acessar imediatamente todos os arquivos de música por meio da biblioteca de músicas.

### <a name="user-data-entry-points"></a>Pontos de entrada de dados do usuário

As bibliotecas padrão (como **meus documentos**, **minhas imagens** e assim por diante) são equivalentes à [pasta conhecida](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). As bibliotecas padrão fornecem pontos de entrada familiares aos usuários, mas como o conteúdo da biblioteca não está limitado a bibliotecas de conteúdo de pastas conhecidas, os usuários dão mais liberdade para determinar onde os documentos e a mídia devem ser armazenados. As bibliotecas são expostas por meio do namespace do Shell (fonte de dados do Shell). Seu aplicativo pode fornecer aos usuários os mesmos pontos de entrada familiares aos dados habilitando o reconhecimento de biblioteca e navegando.

### <a name="collections-of-folders"></a>Coleções de pastas

As bibliotecas são coleções de conteúdo definidas pelo usuário. O Windows Search indexa as pastas com suporte quando elas são incluídas em bibliotecas. Isso permite a pesquisa instantânea e as exibições de disposição de pilha baseadas em Propriedades em bibliotecas.

### <a name="supported-folders-in-libraries"></a>Pastas com suporte em bibliotecas

Para que as pastas tenham suporte em bibliotecas, elas devem ser indexadas no computador local e indexadas em um computador remoto do Windows ou indexadas em um servidor com arquivos indexados pelo Windows Search.

As pastas sem suporte são impedidas de serem adicionadas por usuários na caixa de diálogo gerenciamento de biblioteca do Windows. Se as pastas remotas não indexadas forem adicionadas a uma biblioteca usando a API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) , a experiência do usuário da biblioteca será revertida para o **modo de segurança** da biblioteca. Em recursos de **modo de segurança** , como exibições de disposição de pilha baseada em propriedade, sugestões de filtro e suporte de pesquisa de **menu iniciar** são removidas da biblioteca afetada.

A tabela a seguir lista as pastas incluídas nas bibliotecas usando a caixa de diálogo gerenciamento de biblioteca do Windows Explorer e as pastas que não têm suporte no **modo de segurança**:

| Pastas com suporte                                                                                                                            | Pastas sem suporte                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Discos rígidos NTFS e FAT32 fixos e externos                                                                                                | Unidades removíveis (como thumbdrives e cartões SD)                                                     |
| Compartilhamentos que são indexados pelo Windows Search (como servidores departamentais e em computadores que executam o Windows 10 e o Windows 7 Home Edition) | Mídia removível (como CDs e DVDs)                                                                  |
| Compartilhamentos que estão disponíveis offline (como **meus documentos redirecionados**, **cache do lado do cliente**)                                               | Compartilhamentos de rede que não estão disponíveis offline nem remotamente indexados (como unidades NAS)             |
| N/D                                                                                                                                          | Outras fontes de dados (como Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive e assim por diante) |

### <a name="storage-backed"></a>Storage-Backed

Bibliotecas são coleções de pastas de armazenamento. Os usuários podem salvar e copiar arquivos diretamente em uma biblioteca, já que cada biblioteca tem um local de salvamento padrão para o qual enviar esses arquivos. Para bibliotecas padrão, essa é a pasta conhecida do usuário que está incluída em uma biblioteca (como **meus documentos**) ou a primeira pasta adicionada a uma biblioteca personalizada. Essa é a pasta na qual os arquivos vão quando um usuário arrasta e descarta arquivos em uma biblioteca ou salva em uma biblioteca com a caixa de diálogo arquivo comum. O usuário pode alterar o local de salvamento padrão de uma biblioteca em qualquer ponto, mas se ela remover o local de salvamento padrão, a próxima pasta na biblioteca será selecionada como o novo local de salvamento. Além disso, os usuários podem salvar em qualquer pasta em que eles tenham permissões incluídas em uma biblioteca.

### <a name="non-file-system-shell-containers"></a>Contêineres de shell do sistema não arquivo

As bibliotecas podem conter contêineres do shell do sistema no arquivo, como o **computador** e o **painel de controle**, mas contêm itens do sistema de arquivos. As pastas e o conteúdo da biblioteca podem ser enumerados e acessados usando APIs para arquivos e pastas do sistema de arquivos em sistemas operacionais anteriores. Se seu aplicativo depende muito de APIs específicas do sistema de arquivos, a API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) pode ser usada para obter os caminhos do sistema de arquivos de pastas e arquivos dentro de bibliotecas. Na maioria dos casos, é recomendável que você use o modelo de programação shell para dar suporte a várias versões do Windows e flexibilidade de item. Para obter mais informações, consulte [navegando no namespace do Shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descrições da biblioteca

As descrições de biblioteca são salvas no disco como um arquivo XML na pasta% AppData% Microsoft \\ Windows \\ Libraries (e potencialmente como **\_ bibliotecas FolderId**. Para obter mais informações sobre **\_ bibliotecas FolderId**, consulte [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

Os arquivos de descrição da biblioteca são arquivos XML com a extensão de nome de arquivo. Library-MS. Os arquivos nunca devem ser acessados ou editados por aplicativos. O texto do caminho da pasta persistido para os arquivos de descrição da biblioteca nem sempre é atual. As pastas de biblioteca são mantidas no arquivo de descrição da biblioteca no formato de [links de shell](/windows/desktop/shell/links) binário serializado. Para obter mais informações sobre bibliotecas e o esquema de descrição da biblioteca, consulte o [esquema de descrição da biblioteca](../shell/library-schema-entry.md). Para obter mais informações sobre conectores de pesquisa federada e o esquema de descrição do conector de pesquisa, [pesquise o esquema de descrição do conector](search-sconn-desc-schema-entry.md).

> [OBSERVAÇÃO]  
> Os aplicativos sempre devem usar o modelo de programação shell ou a API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) para consumir e manipular o conteúdo da biblioteca e nunca tentarem acessar manualmente ou editar o arquivo de descrição da biblioteca.

## <a name="related-topics"></a>Tópicos relacionados

[Pesquisa do Windows 7](./-search-3x-wds-overview.md)

[Novo para pesquisa do Windows 7](new-for-windows-7-search.md)

[Priorização de indexação e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md)