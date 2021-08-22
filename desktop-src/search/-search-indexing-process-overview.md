---
description: Este tópico descreve os três estágios do processo de indexação e os principais componentes envolvidos em cada um deles, explica o tempo de atividade de indexação e fornece algumas observações para desenvolvedores de terceiros que desejam que seus armazenamentos de dados ou formatos de arquivo sejam indexados.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: processo de indexação na pesquisa Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5f69306834c001a122a18087205d64b6164d51618226fe0e0fb735f7f5b905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094981"
---
# <a name="indexing-process-in-windows-search"></a>processo de indexação na pesquisa Windows

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

Windows a pesquisa dá suporte à indexação de propriedades e conteúdo de arquivos de formatos de arquivo diferentes, como os formatos .doc ou. jpeg, e armazenamentos de dados, como o sistema de arquivos ou Windows Outlook caixas de correio. Há dois tipos de índices: índices de valor que permitem filtrar e classificar pelo valor inteiro de uma propriedade e índices invertidos que indexam palavras em Propriedades textuais ou conteúdo. se você tiver um formato de arquivo personalizado ou um armazenamento de dados, será necessário entender como Windows índices de pesquisa para que os itens sejam indexados corretamente.

o processo de indexação ocorre em três estágios controlados por um componente de pesquisa Windows chamado de gatherer. No primeiro estágio, o gatherer adiciona URLs às filas. As URLs identificam itens a serem indexados e as filas são meramente listas priorizadas de URLs. no segundo estágio, o coletor coordena outras Windows pesquisa e componentes de terceiros para acessar os itens e coletar dados sobre eles. Por fim, no terceiro estágio, os dados coletados são adicionados ao índice.

O diagrama a seguir mostra os componentes principais e o fluxo de dados por meio do processo de indexação. Vários componentes estão envolvidos na coleta de dados para o índice. algumas delas fazem parte da pesquisa Windows e outras são provenientes de aplicativos de terceiros. se você tiver um armazenamento de dados ou formato de arquivo personalizado, Windows pesquisa se baseia em seu manipulador de protocolo e filtro para acessar URLs e emitir propriedades para indexação. Windows Os componentes de pesquisa são mostrados em azul e os componentes de terceiros são mostrados em verde.

![diagrama mostrando a interação entre os componentes durante o processo de indexação](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Estágio 1: enfileirando URLs para indexação

No primeiro estágio da indexação, o gatherer coleta informações sobre atualizações em armazenamentos de dados, compara essas informações com o escopo de rastreamento conhecido e, em seguida, cria uma fila de URLs para atravessar a coleta de dados para o índice. Para fontes que não são baseadas em notificação, como unidades FAT, o gatherer inicia periodicamente uma passagem completa do escopo do rastreamento para que os dados no índice sejam mantidos atualizados. Para fontes como NTFS, há apenas um único rastreamento e todo o resto é manipulado por notificações do [diário de alterações do USN](/windows/desktop/FileIO/change-journals). Também não há nenhum rastreamento do Microsoft Outlook. O diagrama a seguir mostra uma exibição de alto nível do processo de enfileiramento para indexação sem rastreamento.

![diagrama mostrando o processo de consulta para indexação sem rastreamento](images/queuingurls.jpg)

o restante desta seção explica como Windows pesquisa determina quais URLs rastrear e define alguns termos importantes ao longo do caminho.

**Escopo do rastreamento**  o escopo do rastreamento é um conjunto de URLs que Windows pesquisa percorre para coletar dados sobre os itens que o usuário deseja indexar para pesquisas mais rápidas. Windows A pesquisa adiciona algumas URLs ao escopo de rastreamento por padrão, como caminhos para pastas de **documentos** e **imagens** de usuários. Outras URLs podem ser adicionadas por aplicativos, usuários e Política de Grupo de terceiros. Por fim, os usuários e Política de Grupo podem explicitamente excluir URLs. Windows A pesquisa usa todas as URLs adicionadas e remove as URLs excluídas para determinar o escopo do rastreamento. Esse é o conjunto de trabalho de URLs do qual o coletor inicia seu trabalho.

**Gatherer**  o gatherer é um componente de pesquisa Windows que coleta informações sobre URLs no escopo de rastreamento e cria uma fila de URLs para rastreamento do indexador. Quando um item no escopo de rastreamento é adicionado, excluído ou atualizado, o gatherer é notificado pelo provedor de notificações do repositório de dados. Há um rastreamento inicial no qual o coletor inicia na raiz do escopo do rastreamento. A URL é passada para o manipulador de protocolo e, em seguida, para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)apropriado. O filtro é geralmente uma enumeração de diretório que produz mais URLs. As notificações são o estado estacionário. Normalmente, cada repositório de dados tem seu próprio manipulador de protocolo que fornece essas notificações. Por exemplo, no sistema de arquivos local, o [diário de alterações do USN](/windows/desktop/FileIO/change-journals) atua como um provedor de notificações para todas as URLs no protocolo file://. da mesma forma, o Microsoft Outlook atua como um provedor de notificações para todas as URLs no protocolo mapi://. quando um usuário recebe, move ou exclui email, Outlook notifica o coletor do status alterado do email. A partir dessas notificações, o gatherer cria filas de indexação de URLs para rastreamento.

**Indexando filas**  As filas de indexação são listas de URLs que identificam itens que precisam ser indexados ou reindexados. O coletor compara as URLs que recebe dos provedores de notificações para as URLs no escopo de rastreamento. Cada URL dos provedores de notificações que está dentro do escopo de rastreamento é adicionada a uma fila que o coletor usa para priorizar quais URLs serão processadas em seguida.

Há três filas: notificações de alta prioridade, notificações normais e rastreamentos periódicos. A fila de alta prioridade é para notificações que devem ser processadas imediatamente. por exemplo, quando um usuário altera a propriedade title de um item no Windows explorer, a exibição do Windows Explorer precisa ser atualizada imediatamente após a alteração. A fila de notificação normal é para todas as notificações de alteração restantes. As filas de notificação são processadas antes da fila de rastreamento porque os itens alterados têm maior probabilidade de serem de interesse de um usuário. O coletor acessa dados para as URLs em cada fila na ordem FIFO (primeiro a entrar, primeiro a sair).

para obter mais informações sobre priorização e APIs de eventos introduzidas no Windows 7, consulte [indexação de índices e eventos de conjunto de linhas no Windows 7](indexing-prioritization-and-rowset-events.md). Para obter mais informações sobre o gerenciamento de escopo de rastreamento e notificações, consulte [fornecendo notificações de alteração](-search-3x-wds-notifyingofchanges.md) e [usando o Gerenciador de escopo de rastreamento](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Etapa 2: rastreando URLs

No segundo estágio da indexação, o gatherer rastreia as filas, acessando armazenamentos de dados e recuperando fluxos de itens. Primeiro, o gatherer localiza o manipulador de protocolo apropriado para cada URL. Em seguida, o gatherer passa a URL para o manipulador de protocolo. O manipulador de protocolo acessa o item e passa os metadados de item de volta para o gatherer. O coletor usa os metadados para identificar o filtro correto.

O diagrama a seguir mostra uma exibição de alto nível do processo de rastreamento de URL. Este estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando o processo de rastreamento de URLs e acesso a itens](images/crawlingqueues.jpg)

o restante desta seção descreve como Windows pesquisa acessa itens para indexação e explica as funções de cada um dos componentes envolvidos.

**Gatherer**  No estágio 2, o estágio de rastreamento, o coletor processa as URLs nas filas, começando com a fila de alta prioridade. Cada URL é examinada para identificar seu protocolo. Em seguida, o gatherer pesquisa o manipulador de protocolo registrado para esse protocolo e o instancia no processo de host do protocolo de pesquisa.

**Host de protocolo de pesquisa**  O host de protocolo de pesquisa é meramente um processador, processo de host para manipuladores de protocolo. normalmente, Windows pesquisa cria dois processos de host, um que é executado no contexto de segurança do sistema e outro que é executado no contexto de segurança do usuário. Essa separação garante que os dados específicos para um usuário nunca sejam executados no contexto do sistema.

Windows A pesquisa também usa o processo de host para isolar uma instância de um manipulador de protocolo de outros processos ou aplicativos. Dessa forma, nenhum aplicativo externo pode acessar essa instância específica do manipulador de protocolo e, se o manipulador de protocolo falhar inesperadamente, somente o processo de indexação será afetado. como o processo de host executa código de terceiros (manipuladores de protocolo), Windows pesquisa periodicamente recicla o processo para minimizar o tempo que um ataque bem-sucedido tem de explorar informações no processo. Além disso, o host do protocolo de pesquisa não afeta o rastreamento de URLs ou a indexação de itens.

**Manipuladores de protocolo**  Os manipuladores de protocolo fornecem acesso a itens em um armazenamento de dados usando o protocolo do armazenamento de dados. Por exemplo, o manipulador de protocolo NTFS fornece acesso a arquivos em uma unidade local usando o protocolo file://. O manipulador de protocolo sabe como atravessar o armazenamento de dados, identificar itens novos ou atualizados e notificar o gatherer. Em seguida, quando o rastreamento começa, o manipulador de protocolo fornece um objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) ao coletor para associar ao fluxo subjacente do item e retornar os metadados do item, como restrições de segurança e hora da última modificação.

> [!NOTE]  
> os manipuladores de protocolo não são Windows componentes de pesquisa; Eles são componentes do protocolo e armazenamento de dados específicos que eles são projetados para acessar. Se você tiver um repositório de dados personalizado que deseja indexar, precisará implementar um manipulador de protocolo. Para obter mais informações sobre manipuladores de protocolo e como implementar um, consulte [desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md).

**Metadados e fluxo**  Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o gatherer identifica o filtro correto para a URL. O coletor analisa a extensão de nome de arquivo do item e pesquisa o filtro registrado para essa extensão. se o coletor não conseguir localizar um filtro, Windows pesquisa usará os metadados para derivar um conjunto mínimo de informações de propriedade do sistema (como system. ItemName) e atualizará o índice. Caso contrário, se o gatherer encontrar o filtro, o terceiro estágio de indexação começará.

## <a name="stage-3-updating-the-index"></a>Estágio 3: atualizando o índice

No terceiro estágio da indexação, o gatherer instancia o filtro correto para a URL e inicializa o filtro com o fluxo do objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) . Em seguida, o filtro acessa o item e retorna o conteúdo para o índice. se você tiver um formato de arquivo personalizado, Windows pesquisa se baseia em seu filtro para acessar URLs e emitir conteúdo e propriedades para indexação.

O diagrama a seguir mostra uma exibição de alto nível do processo de acesso a dados. Este estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando os dados de item emitidos para o índice](images/filteringdata.jpg)

O restante desta seção descreve como o Windows Search acessa dados de item para indexação e explica as funções de cada um dos componentes envolvidos.

**Coletor**  No início deste estágio, a função do coletor é insinuar o filtro correto para o item e passá-lo para o fluxo de item. No final deste estágio, o coletor pega o conteúdo e as propriedades emitidas pelo manipulador de filtros e propriedades e atualiza o índice.

**Filtrar Host**  O host de filtro é simplesmente um processo de host para filtros e manipuladores de propriedade e serve para uma finalidade semelhante ao host do protocolo de pesquisa. O processo de host isola filtros e manipuladores de propriedade do restante do sistema pelos mesmos motivos de segurança e estabilidade que os processos de host do protocolo de pesquisa isolam manipuladores de protocolo. O processo de host é executado com direitos mínimos (ele nem mesmo pode acessar o sistema de arquivos) e é ocasionalmente reciclado para proteger contra ataques de segurança. Windows A pesquisa também monitora o uso de recursos para que, se um filtro consumir muitos recursos, o processo de host seja reciclado.

**Filtros**  Os filtros são componentes críticos no processo de indexação que emitem informações de item para o coletor. Os filtros são nomeados após a interface principal usada em sua implementação, a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e, consequentemente, às vezes são chamados de IFilters. Há dois tipos de filtros: um que interage com itens individuais como arquivos e outro que interage com contêineres como pastas. Ambos fornecem dados para o índice.

Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o coletor identifica o filtro correto para uma URL específica e o passa para o fluxo. O coletor identifica o filtro correto por meio de um manipulador de protocolo ou pela extensão de nome de arquivo, tipo MIME ou CLSID (identificador de classe). Se a URL aponta para um contêiner, o filtro emite propriedades para o contêiner e enumera os itens no contêiner (URLs filho). Se a URL aponta para um item, o filtro retorna o conteúdo textual, se qualquer leitura de propriedades e são mais complexas do que manipuladores de propriedade. Em geral, recomendamos que os filtros emitam o conteúdo do item enquanto os manipuladores de propriedades emitem propriedades do item. No entanto, se o filtro precisar funcionar com aplicativos mais antigos que não reconhecem manipuladores de propriedade, você também poderá implementar o filtro para emitir propriedades.

> [!NOTE]  
> Filtros não são componentes Windows Search; eles são componentes relacionados ao formato de arquivo ou contêiner específico que foram projetados para acessar. Para obter mais informações sobre filtros e como implementar um para um contêiner ou formato de arquivo personalizado, consulte Práticas [recomendadas](-search-3x-wds-extidx-filters.md)para criar manipuladores de filtro no Windows Search .

A tabela a seguir lista os resultados que o coletor recebe de um filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e do manipulador de propriedades ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante o processo de indexação.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Permitir gravação**                | Não                                 | Sim                                             |
| **Misturar conteúdo e propriedades** | Sim                                | Não                                              |
| **Multilingue**               | Sim                                | Não                                              |
| **Emitir links**                 | Sim                                | Não                                              |
| **Mime**                       | Sim                                | Não                                              |
| **Limites de texto**            | Frase, parágrafo, capítulo       | Nenhum                                            |
| **Cliente/servidor**            | Ambos                               | Cliente                                          |
| **Implementação**             | Complex                            | Simples                                          |

**Manipuladores de propriedades**  Manipuladores de propriedades são componentes que leem e escrevem propriedades para um formato de arquivo específico. Eles acessam itens e emitem propriedades para o coletor da mesma maneira que os filtros fazem para o conteúdo. Os manipuladores de propriedades são mais fáceis de implementar do que os filtros. Se um formato de arquivo baseado em texto for muito simples ou os arquivos devem ser muito pequenos, o manipulador de propriedades poderá emitir propriedades e conteúdo.

> [!NOTE]  
> Os manipuladores de propriedades não são Windows De pesquisa; eles são componentes relacionados ao formato de arquivo específico que foram projetados para acessar. Para obter mais informações sobre manipuladores de propriedades e como implementar um para um formato de arquivo personalizado, consulte Desenvolvendo manipuladores de propriedades para [Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Propriedades** Windows Search fornece um [sistema de propriedades](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) que inclui uma grande biblioteca de propriedades. Qualquer propriedade pode aparecer em qualquer item, conforme definido pelo filtro ou manipulador de propriedades. Se você tiver um formato de arquivo personalizado, poderá mapear as propriedades do formato de arquivo para essas propriedades do sistema e criar novas propriedades personalizadas. Quando o manipulador de propriedades ou filtro emite essas propriedades, o coletor atualiza o índice para que os usuários possam pesquisar usando suas propriedades. Para obter mais informações sobre como criar e registrar propriedades personalizadas para um formato de arquivo, consulte [Sistema de propriedades](../properties/building-property-handlers.md).

**SystemIndex**  O índice, chamado SystemIndex, armazena dados indexados e é composto por um armazenamento de propriedades e índices sobre as propriedades e o conteúdo das propriedades do item e um índice invertido para conteúdo textual e propriedades. Depois que o coletor atualiza o índice, o índice pode ser consultado por Windows Search e outros aplicativos. Para obter mais informações sobre maneiras de consultar o índice, consulte [Consultando o índice programaticamente.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Lembre-se de que, quando você registra um esquema de novo, as alterações feitas em atributos de propriedades definidas anteriormente podem não ser respeitadas pelo indexador. A solução é recriar o índice ou introduzir novas propriedades que refletem as alterações em vez de atualizar as antigas (não recomendadas). Para obter mais informações, consulte [Observação para implementadores em](#notes-to-implementers) Visão geral do sistema de [propriedades](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Como a indexação é agendada

Quando Windows Search é instalado pela primeira vez, ele executa uma indexação completa do escopo de rastreamento, pausando durante períodos de alta E/S e atividade do usuário. O escopo de rastreamento padrão consiste nos locais de biblioteca padrão, como **Documentos,** **Música,** **Imagens** e **Vídeos.** As notificações são processadas mesmo antes que o rastreamento inicial seja concluído. Ocasionalmente, o coletor rastrea as URLs do escopo de rastreamento completo. Esses rastreamentos completos garantem que os dados no índice estão atualizados. Por exemplo, se um provedor de notificação não enviar notificações ou se o Windows serviço Pesquisa for encerrado inesperadamente, o coletor não terá conhecimento de itens novos ou alterados e não indexará esses itens. Há dois tipos de fontes: somente notificação e notificação habilitada. Em ambas as fontes, o coletor rastrea inicialmente o índice. Após o rastreamento inicial, as fontes somente notificação nunca fazerão um rastreamento completo novamente, a menos que haja uma falha, como a rolagem do Diário de Alterações da [USN.](/windows/desktop/FileIO/change-journals) As fontes habilitadas para notificação fazem um rastreamento incremental quando o indexador é iniciado, mas escutam as notificações durante a execução. NTFS e Microsoft Outlook são somente notificação. Internet Explorer e FAT estão habilitados para notificação.

## <a name="notes-to-implementers"></a>Notas aos Implementadores

A qualidade dos dados no índice e a eficiência do processo de indexação dependem muito da implementação do filtro e do manipulador de propriedades. Como o filtro é chamado sempre que uma URL identifica o formato de arquivo, o processo de indexação pode diminuir drasticamente se o filtro for ineficiente. Se o manipulador de propriedades não mapear corretamente todas as propriedades de arquivo para as propriedades do sistema ou não emitir corretamente essas propriedades, os dados no índice estarão incorretos e pesquisas posteriores para essas propriedades retornarão resultados incorretos. Se o filtro ou o manipulador de propriedades falhar, o indexador não poderá indexar dados.

Aplicativos e processos diferentes do Windows Search dependem de manipuladores de protocolo, filtros e manipuladores de propriedade. Suas implementações podem afetar esses aplicativos de maneiras que talvez você não espere. O [guia Windows desenvolvimento de pesquisa](-search-developers-guide-entry-page.md) de dados fornece conselhos sobre opções de design e sobre como testar cada um desses componentes.

## <a name="related-topics"></a>Tópicos relacionados

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)

[O que está incluído no índice](-search-indexing-process-overview.md)

[Processo de consulta na Windows Search](querying-process--windows-search-.md)

[Processo de notificações na Windows Search](-search-3x-wds-support.md)

[Requisitos de formatação de URL](url-formatting-requirements.md)
