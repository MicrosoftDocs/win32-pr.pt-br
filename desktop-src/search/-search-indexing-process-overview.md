---
description: Este tópico descreve os três estágios do processo de indexação e os principais componentes envolvidos em cada um deles, explica o tempo de atividade de indexação e fornece algumas observações para desenvolvedores de terceiros que desejam que seus armazenamentos de dados ou formatos de arquivo sejam indexados.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Processo de indexação no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87867d5925cd53b237092435bbc9d16428418b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646875"
---
# <a name="indexing-process-in-windows-search"></a>Processo de indexação no Windows Search

Este tópico descreve os três estágios do processo de indexação e os principais componentes envolvidos em cada um deles, explica o tempo de atividade de indexação e fornece algumas observações para desenvolvedores de terceiros que desejam que seus armazenamentos de dados ou formatos de arquivo sejam indexados.

Este tópico é organizado da seguinte maneira:

- [Visão geral](#overview)
- [Estágio 1: enfileirando URLs para indexação](#stage-1-queuing-urls-for-indexing)
- [Etapa 2: rastreando URLs](#stage-2-crawling-urls)
- [Estágio 3: atualizando o índice](#stage-3-updating-the-index)
- [Como a indexação é agendada](#how-indexing-is-scheduled)
- [Notas aos Implementadores](#notes-to-implementers)
- [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

O Windows Search dá suporte à indexação de propriedades e conteúdo de arquivos de formatos de arquivo diferentes, como formatos. doc ou. jpeg e armazenamentos de dados, como o sistema de arquivos ou as caixas de correio do Windows Outlook. Há dois tipos de índices: índices de valor que permitem filtrar e classificar pelo valor inteiro de uma propriedade e índices invertidos que indexam palavras em Propriedades textuais ou conteúdo. Se você tiver um formato de arquivo personalizado ou um armazenamento de dados, você precisará entender como os índices do Windows Search para que os itens sejam indexados corretamente.

O processo de indexação ocorre em três estágios controlados por um componente de pesquisa do Windows chamado gatherer. No primeiro estágio, o gatherer adiciona URLs às filas. As URLs identificam itens a serem indexados e as filas são meramente listas priorizadas de URLs. No segundo estágio, o coletor coordena outras pesquisas do Windows e componentes de terceiros para acessar os itens e coletar dados sobre eles. Por fim, no terceiro estágio, os dados coletados são adicionados ao índice.

O diagrama a seguir mostra os componentes principais e o fluxo de dados por meio do processo de indexação. Vários componentes estão envolvidos na coleta de dados para o índice. Algumas delas fazem parte do Windows Search e algumas vêm de aplicativos de terceiros. Se você tiver um armazenamento de dados ou formato de arquivo personalizado, o Windows Search dependerá de seu manipulador de protocolo e filtro para acessar URLs e emitir Propriedades para indexação. Os componentes do Windows Search são mostrados em azul e os componentes de terceiros são mostrados em verde.

![diagrama mostrando a interação entre os componentes durante o processo de indexação](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Estágio 1: enfileirando URLs para indexação

No primeiro estágio da indexação, o gatherer coleta informações sobre atualizações em armazenamentos de dados, compara essas informações com o escopo de rastreamento conhecido e, em seguida, cria uma fila de URLs para atravessar a coleta de dados para o índice. Para fontes que não são baseadas em notificação, como unidades FAT, o gatherer inicia periodicamente uma passagem completa do escopo do rastreamento para que os dados no índice sejam mantidos atualizados. Para fontes como NTFS, há apenas um único rastreamento e todo o resto é manipulado por notificações do [diário de alterações do USN](/windows/desktop/FileIO/change-journals). Também não há nenhum rastreamento do Microsoft Outlook. O diagrama a seguir mostra uma exibição de alto nível do processo de enfileiramento para indexação sem rastreamento.

![diagrama mostrando o processo de consulta para indexação sem rastreamento](images/queuingurls.jpg)

O restante desta seção explica como o Windows Search determina quais URLs rastrear e define alguns termos importantes ao longo do caminho.

**Escopo do rastreamento**  O escopo do rastreamento é um conjunto de URLs que o Windows Search percorre para coletar dados sobre os itens que o usuário deseja indexar para pesquisas mais rápidas. O Windows Search adiciona algumas URLs ao escopo de rastreamento por padrão, como caminhos para pastas de **documentos** e **imagens** de usuários. Outras URLs podem ser adicionadas por aplicativos, usuários e Política de Grupo de terceiros. Por fim, os usuários e Política de Grupo podem explicitamente excluir URLs. O Windows Search usa todas as URLs adicionadas e remove as URLs excluídas para determinar o escopo do rastreamento. Esse é o conjunto de trabalho de URLs do qual o coletor inicia seu trabalho.

**Gatherer**  O gatherer é um componente de pesquisa do Windows que coleta informações sobre URLs no escopo do rastreamento e cria uma fila de URLs para rastreamento do indexador. Quando um item no escopo de rastreamento é adicionado, excluído ou atualizado, o gatherer é notificado pelo provedor de notificações do repositório de dados. Há um rastreamento inicial no qual o coletor inicia na raiz do escopo do rastreamento. A URL é passada para o manipulador de protocolo e, em seguida, para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)apropriado. O filtro é geralmente uma enumeração de diretório que produz mais URLs. As notificações são o estado estacionário. Normalmente, cada repositório de dados tem seu próprio manipulador de protocolo que fornece essas notificações. Por exemplo, no sistema de arquivos local, o [diário de alterações do USN](/windows/desktop/FileIO/change-journals) atua como um provedor de notificações para todas as URLs no protocolo file://. Da mesma forma, o Microsoft Outlook atua como um provedor de notificações para todas as URLs no protocolo mapi://. Quando um usuário recebe, move ou exclui email, o Outlook notifica o gatherer sobre o status alterado do email. A partir dessas notificações, o gatherer cria filas de indexação de URLs para rastreamento.

**Indexando filas**  As filas de indexação são listas de URLs que identificam itens que precisam ser indexados ou reindexados. O coletor compara as URLs que recebe dos provedores de notificações para as URLs no escopo de rastreamento. Cada URL dos provedores de notificações que está dentro do escopo de rastreamento é adicionada a uma fila que o coletor usa para priorizar quais URLs serão processadas em seguida.

Há três filas: notificações de alta prioridade, notificações normais e rastreamentos periódicos. A fila de alta prioridade é para notificações que devem ser processadas imediatamente. Por exemplo, quando um usuário altera a propriedade Title de um item no Windows Explorer, o modo de exibição do Windows Explorer precisa ser atualizado imediatamente após a alteração. A fila de notificação normal é para todas as notificações de alteração restantes. As filas de notificação são processadas antes da fila de rastreamento porque os itens alterados têm maior probabilidade de serem de interesse de um usuário. O coletor acessa dados para as URLs em cada fila na ordem FIFO (primeiro a entrar, primeiro a sair).

Para obter mais informações sobre priorização e APIs de eventos introduzidas no Windows 7, consulte [indexação de índices e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md). Para obter mais informações sobre o gerenciamento de escopo de rastreamento e notificações, consulte [fornecendo notificações de alteração](-search-3x-wds-notifyingofchanges.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Etapa 2: rastreando URLs

No segundo estágio da indexação, o gatherer rastreia as filas, acessando armazenamentos de dados e recuperando fluxos de itens. Primeiro, o gatherer localiza o manipulador de protocolo apropriado para cada URL. Em seguida, o gatherer passa a URL para o manipulador de protocolo. O manipulador de protocolo acessa o item e passa os metadados de item de volta para o gatherer. O coletor usa os metadados para identificar o filtro correto.

O diagrama a seguir mostra uma exibição de alto nível do processo de rastreamento de URL. Este estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando o processo de rastreamento de URLs e acesso a itens](images/crawlingqueues.jpg)

O restante desta seção descreve como o Windows Search acessa itens para indexação e explica as funções de cada um dos componentes envolvidos.

**Gatherer**  No estágio 2, o estágio de rastreamento, o coletor processa as URLs nas filas, começando com a fila de alta prioridade. Cada URL é examinada para identificar seu protocolo. Em seguida, o gatherer pesquisa o manipulador de protocolo registrado para esse protocolo e o instancia no processo de host do protocolo de pesquisa.

**Host de protocolo de pesquisa**  O host de protocolo de pesquisa é meramente um processador, processo de host para manipuladores de protocolo. Normalmente, o Windows Search cria dois processos de host, um que é executado no contexto de segurança do sistema e um que é executado no contexto de segurança do usuário. Essa separação garante que os dados específicos para um usuário nunca sejam executados no contexto do sistema.

O Windows Search também usa o processo de host para isolar uma instância de um manipulador de protocolo de outros processos ou aplicativos. Dessa forma, nenhum aplicativo externo pode acessar essa instância específica do manipulador de protocolo e, se o manipulador de protocolo falhar inesperadamente, somente o processo de indexação será afetado. Como o processo de host executa código de terceiros (manipuladores de protocolo), o Windows Search recicla periodicamente o processo para minimizar o tempo que um ataque bem-sucedido tem de explorar informações no processo. Além disso, o host do protocolo de pesquisa não afeta o rastreamento de URLs ou a indexação de itens.

**Manipuladores de protocolo**  Os manipuladores de protocolo fornecem acesso a itens em um armazenamento de dados usando o protocolo do armazenamento de dados. Por exemplo, o manipulador de protocolo NTFS fornece acesso a arquivos em uma unidade local usando o protocolo file://. O manipulador de protocolo sabe como atravessar o armazenamento de dados, identificar itens novos ou atualizados e notificar o gatherer. Em seguida, quando o rastreamento começa, o manipulador de protocolo fornece um objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) ao coletor para associar ao fluxo subjacente do item e retornar os metadados do item, como restrições de segurança e hora da última modificação.

> [!NOTE]  
> Os manipuladores de protocolo não são componentes do Windows Search; Eles são componentes do protocolo e armazenamento de dados específicos que eles são projetados para acessar. Se você tiver um repositório de dados personalizado que deseja indexar, precisará implementar um manipulador de protocolo. Para obter mais informações sobre manipuladores de protocolo e como implementar um, consulte [desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md).

**Metadados e fluxo**  Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o gatherer identifica o filtro correto para a URL. O coletor analisa a extensão de nome de arquivo do item e pesquisa o filtro registrado para essa extensão. Se o coletor não conseguir localizar um filtro, o Windows Search usará os metadados para derivar um conjunto mínimo de informações de Propriedade do sistema (como System. ItemName) e atualizará o índice. Caso contrário, se o gatherer encontrar o filtro, o terceiro estágio de indexação começará.

## <a name="stage-3-updating-the-index"></a>Estágio 3: atualizando o índice

No terceiro estágio da indexação, o gatherer instancia o filtro correto para a URL e inicializa o filtro com o fluxo do objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) . Em seguida, o filtro acessa o item e retorna o conteúdo para o índice. Se você tiver um formato de arquivo personalizado, o Windows Search dependerá de seu filtro para acessar URLs e emitir o conteúdo e as propriedades para indexação.

O diagrama a seguir mostra uma exibição de alto nível do processo de acesso a dados. Este estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando os dados do item emitidos para o índice](images/filteringdata.jpg)

O restante desta seção descreve como o Windows Search acessa os dados de item para indexação e explica as funções de cada um dos componentes envolvidos.

**Gatherer**  No início deste estágio, a função do coletor é criar uma instância do filtro correto para o item e passá-lo para o fluxo do item. No final deste estágio, o coletor pega o conteúdo e as propriedades emitidos pelo manipulador de propriedades e pelo filtro e atualiza o índice.

**Host de filtro**  O host de filtro é meramente um processo de host para filtros e manipuladores de propriedade e atende a uma finalidade semelhante ao host de protocolo de pesquisa. O processo de host isola filtros e manipuladores de Propriedade do restante do sistema para os mesmos motivos de segurança e estabilidade que os processos de host de protocolo de pesquisa isolam os manipuladores de protocolo. O processo de host é executado com direitos mínimos (ele não pode até mesmo acessar o sistema de arquivos) e, ocasionalmente, é reciclado para proteger contra ataques de segurança. O Windows Search também monitora o uso de recursos para que, se um filtro consumir muitos recursos, o processo do host seja reciclado.

**Filtros**  do  Filtros são componentes críticos no processo de indexação que emitem informações de itens para o gatherer. Os filtros são nomeados após a interface principal usada em sua implementação, a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e, consequentemente, são chamados de IFilters. Há dois tipos de filtros: um que interage com itens individuais como arquivos e outro que interage com contêineres como pastas. Ambos fornecem dados para o índice.

Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o coletor identifica o filtro correto para uma URL específica e o passa para o fluxo. O coletor identifica o filtro correto por meio de um manipulador de protocolo ou pela extensão de nome de arquivo, tipo de MIME ou identificador de classe (CLSID). Se a URL apontar para um contêiner, o filtro emitirá as propriedades para o contêiner e enumerará os itens no contêiner (URLs filho). Se a URL apontar para um item, o filtro retornará o conteúdo textual, se qualquer leitura de propriedades e for mais complexa que os manipuladores de propriedade. Em geral, recomendamos que os filtros emitam o conteúdo do item enquanto os manipuladores de propriedade emitirem Propriedades de item. No entanto, se o filtro precisar trabalhar com aplicativos mais antigos que não reconheçam manipuladores de propriedade, você também poderá implementar o filtro para emitir Propriedades.

> [!NOTE]  
> Os filtros não são componentes do Windows Search; Eles são componentes relacionados ao formato ou ao contêiner de arquivo específico que eles são projetados para acessar. Para obter mais informações sobre filtros e como implementar um para um formato ou contêiner de arquivo personalizado, consulte [práticas recomendadas para criar manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md).

A tabela a seguir lista os resultados que o coletor recebe de um filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e um manipulador de Propriedades ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante o processo de indexação.

|                            | [**Visio**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| Permitir gravação                | Não                                 | Sim                                             |
| Misturar conteúdo e propriedades | Sim                                | Não                                              |
| Multilíngüe               | Sim                                | Não                                              |
| Links de emissão                 | Sim                                | Não                                              |
| MIME                       | Sim                                | Não                                              |
| Limites de texto            | Sentença, parágrafo, capítulo       | Nenhum                                            |
| Cliente/servidor            | Ambos                               | Cliente                                          |
| Implementação             | Complex                            | Simples                                          |

**Manipuladores de propriedade**  Manipuladores de propriedade são componentes que lêem e gravam Propriedades para um determinado formato de arquivo. Eles acessam itens e as propriedades de emissão do coletor da mesma maneira que os filtros fazem para o conteúdo. Manipuladores de propriedade são mais fáceis de implementar do que filtros. Se um formato de arquivo baseado em texto for muito simples ou se for esperado que os arquivos sejam muito pequenos, o manipulador de propriedades poderá emitir as propriedades e o conteúdo.

> [!NOTE]  
> Manipuladores de propriedade não são componentes do Windows Search; Eles são componentes relacionados ao formato de arquivo específico que eles são projetados para acessar. Para obter mais informações sobre manipuladores de propriedade e como implementar um para um formato de arquivo personalizado, consulte [desenvolvendo manipuladores de propriedade para o Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Propriedades** do O Windows Search fornece um [sistema de propriedades](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) que inclui uma grande biblioteca de propriedades. Qualquer propriedade pode aparecer em qualquer item, conforme definido pelo manipulador de filtro ou propriedade. Se você tiver um formato de arquivo personalizado, poderá mapear as propriedades do formato de arquivo para essas propriedades do sistema e poderá criar novas propriedades personalizadas. Quando o seu manipulador de filtro ou Propriedade emite essas propriedades, o gatherer atualiza o índice para que os usuários possam Pesquisar usando suas propriedades. Para obter mais informações sobre como criar e registrar Propriedades personalizadas para um formato de arquivo, consulte [sistema de propriedades](../properties/building-property-handlers.md).

**SystemIndex**  O índice, chamado SystemIndex, armazena dados indexados e é composto de um repositório de propriedades e de índices sobre as propriedades e o conteúdo de propriedades de item e um índice invertido para conteúdo e propriedades textuais. Depois que o gatherer atualizar o índice, o índice poderá ser consultado pelo Windows Search e por outros aplicativos. Para obter mais informações sobre maneiras de consultar o índice, consulte [consultando o índice programaticamente](-search-3x-wds-qryidx-overview.md).

> [!NOTE]  
> Lembre-se de que quando você registra novamente um esquema, as alterações feitas em atributos de propriedades definidas anteriormente podem não ser respeitadas pelo indexador. A solução é recriar o índice ou introduzir novas propriedades que reflitam as alterações em vez de atualizar as antigas (não recomendado). Para obter mais informações, consulte [Observação para implementadores](#notes-to-implementers) em [Propriedades visão geral do sistema](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Como a indexação é agendada

Quando o Windows Search é instalado pela primeira vez, ele executa uma indexação completa do escopo do rastreamento, pausa durante períodos de alta atividade de e/s e de usuário. O escopo de rastreamento padrão consiste em locais de biblioteca padrão, como **documentos**, **música**, **imagens** e **vídeos**. As notificações são processadas mesmo antes de o rastreamento inicial ser concluído. Ocasionalmente, o coletor rastreia as URLs do escopo de rastreamento completo. Esses rastreamentos completos garantem que os dados no índice sejam atualizados. Por exemplo, se um provedor de notificação não conseguir enviar notificações ou se o serviço de pesquisa do Windows for finalizado inesperadamente, o coletor não teria conhecimento de itens novos ou alterados e não indexaria esses itens. Há dois tipos de fontes: somente notificação e notificação habilitada. Em ambas as fontes, o gatherer inicialmente rastreia o índice. Após o rastreamento inicial, as fontes somente notificação nunca farão um rastreamento completo novamente, a menos que haja uma falha, como o [diário de alterações do USN](/windows/desktop/FileIO/change-journals) que está sendo revertida. As fontes habilitadas para notificação fazem um rastreamento incremental quando o indexador é iniciado, mas depois ouve as notificações durante a execução. O NTFS e o Microsoft Outlook são somente notificação. O Internet Explorer e o FAT estão habilitados para notificação.

## <a name="notes-to-implementers"></a>Notas aos Implementadores

A qualidade dos dados no índice e a eficiência do processo de indexação dependem muito do filtro e da implementação do manipulador de propriedade. Como o filtro é chamado toda vez que uma URL identifica o formato de arquivo, o processo de indexação pode diminuir drasticamente se o filtro não for eficiente. Se o manipulador de propriedades não mapear corretamente todas as propriedades de arquivo para propriedades do sistema ou não emitir corretamente essas propriedades, os dados no índice ficarão incorretos e as pesquisas posteriores para essas propriedades retornarão resultados incorretos. Se o filtro ou o manipulador de propriedades falhar, o indexador não poderá indexar dados.

Aplicativos e processos que não sejam o Windows Search dependem de manipuladores de protocolo, filtros e manipuladores de propriedades. Suas implementações podem afetar esses aplicativos de maneiras que você talvez não espere. O [Guia de desenvolvimento do Windows Search](-search-developers-guide-entry-page.md) fornece conselhos sobre opções de design e sobre como testar cada um desses componentes.

## <a name="related-topics"></a>Tópicos relacionados

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)

[O que está incluído no índice](-search-indexing-process-overview.md)

[Processo de consulta no Windows Search](querying-process--windows-search-.md)

[Processo de notificações no Windows Search](-search-3x-wds-support.md)

[Requisitos de formatação de URL](url-formatting-requirements.md)
