---
description: Este tópico descreve os três estágios do processo de indexação e os componentes principais envolvidos em cada um, explica o tempo da atividade de indexação e fornece algumas observações para desenvolvedores de terceiros que querem que seus armazenamentos de dados ou formatos de arquivo sejam indexados.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Processo de indexação em Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b819a056b9a3dd44ea799ee56ae6b2e87606f552
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119531"
---
# <a name="indexing-process-in-windows-search"></a>Processo de indexação em Windows Search

Este tópico descreve os três estágios do processo de indexação e os componentes principais envolvidos em cada um, explica o tempo da atividade de indexação e fornece algumas observações para desenvolvedores de terceiros que querem que seus armazenamentos de dados ou formatos de arquivo sejam indexados.

Este tópico é organizado da seguinte forma:

- [Visão geral](#overview)
- [Estágio 1: UrLs de enxuamento para indexação](#stage-1-queuing-urls-for-indexing)
- [Estágio 2: URLs de rastreamento](#stage-2-crawling-urls)
- [Estágio 3: Atualizando o índice](#stage-3-updating-the-index)
- [Como a indexação é agendada](#how-indexing-is-scheduled)
- [Notas aos Implementadores](#notes-to-implementers)
- [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Windows Search dá suporte à indexação de propriedades e conteúdo de arquivos de formatos de arquivo diferentes, como formatos .doc ou .jpeg e armazenamentos de dados, como o sistema de arquivos ou caixas de correio do Windows Outlook. Há dois tipos de índices: índices de valor que permitem filtrar e classificar pelo valor inteiro de uma propriedade e índices invertidos que indexam palavras em propriedades textuais ou conteúdo. Se você tiver um formato de arquivo personalizado ou um armazenamento de dados, precisará entender como Windows Search índices para que seus itens indexem corretamente.

O processo de indexação ocorre em três estágios controlado por Windows Search componente chamado coletor. No primeiro estágio, o coletor adiciona URLs às filas. As URLs identificam os itens a serem indexados e as filas são simplesmente listas priorizadas de URLs. No segundo estágio, o coletor coordena outros Windows Search e componentes de terceiros para acessar os itens e coletar dados sobre eles. Por fim, no terceiro estágio, os dados coletados são adicionados ao índice.

O diagrama a seguir mostra os componentes principais e o fluxo de dados por meio do processo de indexação. Vários componentes estão envolvidos na coleta de dados para o índice. Alguns deles fazem parte do Windows Search e alguns vêm de aplicativos de terceiros. Se você tiver um armazenamento de dados personalizado ou formato de arquivo, Windows Search depende do manipulador de protocolo e do filtro para acessar URLs e emitir propriedades para indexação. Windows Search componentes são mostrados em azul e componentes de terceiros são mostrados em verde.

![diagrama mostrando a interação entre componentes durante o processo de indexação](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Estágio 1: UrLs de enxuamento para indexação

No primeiro estágio de indexação, o coletor coleta informações sobre atualizações para armazenamentos de dados, compara essas informações com o escopo de rastreamento conhecido e, em seguida, cria uma fila de URLs para percorrer para coletar dados para o índice. Para fontes que não se baseiam na notificação, como unidades FAT, o coletor inicia periodicamente uma travessia completa do escopo de rastreamento para que os dados no índice sejam mantidos atualizados. Para fontes como NTFS, há apenas um único rastreamento e todo o resto é tratado por notificações do [UsN Change Journal](/windows/desktop/FileIO/change-journals). Também não há rastreamento do Microsoft Outlook. O diagrama a seguir mostra uma exibição de alto nível do processo de enxuamento para indexação não rastreada.

![diagrama mostrando o processo de consulta para indexação não rastreada](images/queuingurls.jpg)

O restante desta seção explica como Windows Search quais URLs rastrear e define alguns termos importantes ao longo do caminho.

**Escopo do rastreamento**  O escopo de rastreamento é um conjunto de URLs que Windows Search para coletar dados sobre itens que o usuário deseja indexar para pesquisas mais rápidas. Windows Search adiciona algumas URLs ao escopo de rastreamento por padrão, como caminhos para as pastas **Documentos** **e** Imagens dos usuários. Outras URLs podem ser adicionadas por aplicativos, usuários e Política de Grupo. Por fim, os usuários e Política de Grupo podem excluir explicitamente URLs. Windows Search todas as URLs adicionadas e remove as URLs excluídas para determinar o escopo do rastreamento. Esse é o conjunto de trabalho de URLs do qual o coletor começa seu trabalho.

**Coletor**  O coletor é um Windows Search que coleta informações sobre URLs dentro do escopo de rastreamento e cria uma fila de URLs para o indexador rastrear. Quando um item no escopo de rastreamento é adicionado, excluído ou atualizado, o coletor é notificado pelo provedor de notificações do armazenamento de dados. Há um rastreamento inicial em que o coletor começa na raiz do escopo do rastreamento. A URL é passada para o manipulador de protocolo e, em seguida, para o [**IFilter apropriado.**](/windows/win32/api/filter/nn-filter-ifilter) O filtro geralmente é uma enumeração de diretório que produz mais URLs. As notificações são o estado estável. Normalmente, cada armazenamento de dados tem seu próprio manipulador de protocolo que fornece essas notificações. Por exemplo, no sistema de arquivos local, o Diário de Alterações do [USN](/windows/desktop/FileIO/change-journals) atua como um provedor de notificações para todas as URLs no protocolo file://. Da mesma forma, o Microsoft Outlook atua como um provedor de notificações para todas as URLs no mapi:// protocolo. Quando um usuário recebe, move ou exclui email, o Outlook notifica o coletor do status alterado do email. Com base nessas notificações, o coletor cria filas de indexação de URLs para rastreamento.

**Filas de indexação**  As filas de indexação são listas de URLs que identificam itens que precisam ser indexados ou indexados. O coletor compara as URLs recebidas dos provedores de notificações com as URLs no escopo do rastreamento. Cada URL de provedores de notificações que está dentro do escopo de rastreamento é adicionada a uma fila que o coletor usa para priorizar quais URLs processar em seguida.

Há três filas: notificações de alta prioridade, notificações normais e rastreamentos periódicos. A fila de alta prioridade é para notificações que devem ser processadas imediatamente. Por exemplo, quando um usuário altera a propriedade de título de um item no Windows Explorer, o Windows Explorer exibição precisa ser atualizado imediatamente após a alteração. A fila de notificação normal é para todas as notificações de alteração restantes. As filas de notificação são processadas antes da fila de rastreamento porque os itens alterados têm maior probabilidade de serem de interesse de um usuário. O coletor acessa dados para as URLs em cada fila na ordem FIFO (primeiro a entrar, primeiro a sair).

Para obter mais informações sobre priorização e APIs de eventos introduzidas no Windows 7, consulte Indexando priorização e eventos de conjuntos [de linhas no Windows 7](indexing-prioritization-and-rowset-events.md). Para obter mais informações sobre o gerenciamento de escopo de rastreamento e notificações, consulte [Fornecendo](-search-3x-wds-notifyingofchanges.md) notificações de alteração e [usando o Gerenciador do Escopo de Rastreamento](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Estágio 2: URLs de rastreamento

No segundo estágio de indexação, o coletor passa pelas filas, acessando armazenamentos de dados e recuperando fluxos de itens. Primeiro, o coletor localiza o manipulador de protocolo apropriado para cada URL. Em seguida, o coletor passa a URL para o manipulador de protocolo. O manipulador de protocolo acessa o item e passa os metadados do item de volta para o coletor. O coletor usa os metadados para identificar o filtro correto.

O diagrama a seguir mostra uma exibição de alto nível do processo de rastreamento de URL. Esse estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando o processo de rastreamento de URLs e acesso a itens](images/crawlingqueues.jpg)

O restante desta seção descreve como o Windows Search acessa itens para indexação e explica as funções de cada um dos componentes envolvidos.

**Coletor**  No estágio 2, o estágio de rastreamento, o coletor processa as URLs nas filas, começando com a fila de alta prioridade. Cada URL é examinada para identificar seu protocolo. Em seguida, o coletor pesquisa o manipulador de protocolo registrado para esse protocolo e o instalita no processo de host do protocolo de pesquisa.

**Host do Protocolo de Pesquisa**  O host do protocolo de pesquisa é simplesmente um processo de host de caixa para manipuladores de protocolo. Normalmente, Windows Search cria dois desses processos de host, um que é executado no contexto de segurança do sistema e outro que é executado no contexto de segurança do usuário. Essa separação garante que os dados específicos de um usuário nunca são executados no contexto do sistema.

Windows Search também usa o processo de host para isolar uma instância de um manipulador de protocolo de outros processos ou aplicativos. Dessa forma, nenhum aplicativo externo pode acessar essa instância específica do manipulador de protocolo e, se o manipulador de protocolo falhar inesperadamente, somente o processo de indexação será afetado. Como o processo de host executa código de terceiros (manipuladores de protocolo), o Windows Search recicla periodicamente o processo para minimizar o tempo que um ataque bem-sucedido tem para explorar informações no processo. Além disso, o host do protocolo de pesquisa não afeta o rastreamento de URLs ou a indexação de itens.

**Manipuladores de protocolo**  Os manipuladores de protocolo fornecem acesso a itens em um armazenamento de dados usando o protocolo do armazenamento de dados. Por exemplo, o manipulador de protocolo NTFS fornece acesso a arquivos em uma unidade local usando o file:// protocolo. O manipulador de protocolo sabe como percorrer o armazenamento de dados, identificar itens novos ou atualizados e notificar o coletor. Em seguida, quando o rastreamento começa, o manipulador de protocolo fornece um objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) ao coletor para se vincular ao fluxo subjacente do item e retornar metadados de item, como restrições de segurança e hora da última modificação.

> [!NOTE]  
> Manipuladores de protocolo não são Windows Search componentes; eles são componentes do protocolo específico e do armazenamento de dados que foram projetados para acessar. Se você tiver um armazenamento de dados personalizado que deseja indexar, será necessário implementar um manipulador de protocolo. Para obter mais informações sobre manipuladores de protocolo e como implementar um, consulte [Desenvolvendo manipuladores de protocolo](-search-3x-wds-phaddins.md).

**Metadados e fluxo**  Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o coletor identifica o filtro correto para a URL. O coletor analisa a extensão de nome de arquivo do item e procura o filtro registrado para essa extensão. Se o coletor não conseguir encontrar um filtro, o Windows Search usará os metadados para derivar um conjunto mínimo de informações de propriedade do sistema (como System.ItemName) e atualizará o índice. Caso contrário, se o coletor encontrar o filtro, o terceiro estágio da indexação começará.

## <a name="stage-3-updating-the-index"></a>Estágio 3: Atualizando o índice

No terceiro estágio de indexação, o coletor instalita o filtro correto para a URL e inicializa o filtro com o fluxo do objeto [**IUrlAccessor.**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) Em seguida, o filtro acessa o item e retorna conteúdo para o índice. Se você tiver um formato de arquivo personalizado, Windows Search depende do filtro para acessar URLs e emitir conteúdo e propriedades para indexação.

O diagrama a seguir mostra uma exibição de alto nível do processo de acesso a dados. Esse estágio inclui coordenação considerável e comunicação entre componentes.

![diagrama mostrando os dados de item emitidos para o índice](images/filteringdata.jpg)

O restante desta seção descreve como o Windows Search dados de item para indexação e explica as funções de cada um dos componentes envolvidos.

**Coletor**  No início deste estágio, a função do coletor é insinuar o filtro correto para o item e passá-lo para o fluxo de item. No final deste estágio, o coletor pega o conteúdo e as propriedades emitidas pelo manipulador de filtros e propriedades e atualiza o índice.

**Filtrar Host**  O host de filtro é simplesmente um processo de host para filtros e manipuladores de propriedade e serve para uma finalidade semelhante ao host do protocolo de pesquisa. O processo de host isola filtros e manipuladores de propriedade do restante do sistema pelos mesmos motivos de segurança e estabilidade que os processos de host do protocolo de pesquisa isolam manipuladores de protocolo. O processo de host é executado com direitos mínimos (ele nem mesmo pode acessar o sistema de arquivos) e é ocasionalmente reciclado para proteger contra ataques de segurança. Windows Search também monitora o uso de recursos para que, se um filtro consumir muitos recursos, o processo de host seja reciclado.

**Filtros**  Os filtros são componentes críticos no processo de indexação que emitem informações de item para o coletor. Os filtros são nomeados após a interface principal usada em sua implementação, a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e, consequentemente, às vezes são chamados de IFilters. Há dois tipos de filtros: um que interage com itens individuais como arquivos e outro que interage com contêineres como pastas. Ambos fornecem dados para o índice.

Usando metadados retornados pelo objeto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) do manipulador de protocolo, o coletor identifica o filtro correto para uma URL específica e o passa para o fluxo. O coletor identifica o filtro correto por meio de um manipulador de protocolo ou pela extensão de nome de arquivo, tipo MIME ou CLSID (identificador de classe). Se a URL aponta para um contêiner, o filtro emite propriedades para o contêiner e enumera os itens no contêiner (URLs filho). Se a URL aponta para um item, o filtro retorna o conteúdo textual, se qualquer leitura de propriedades e são mais complexas do que manipuladores de propriedade. Em geral, recomendamos que os filtros emitam o conteúdo do item enquanto os manipuladores de propriedades emitem propriedades do item. No entanto, se o filtro precisar funcionar com aplicativos mais antigos que não reconhecem manipuladores de propriedades, você também poderá implementar o filtro para emitir propriedades.

> [!NOTE]  
> Filtros não são Windows Search componentes; eles são componentes relacionados ao formato de arquivo ou contêiner específico que foram projetados para acessar. Para obter mais informações sobre filtros e como implementar um para um formato de arquivo personalizado ou contêiner, consulte Práticas [recomendadas](-search-3x-wds-extidx-filters.md)para criar manipuladores de filtro no Windows Search .

A tabela a seguir lista os resultados que o coletor recebe de um filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e do manipulador de propriedades ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante o processo de indexação.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Permitir gravação**                | Não                                 | Sim                                             |
| **Misturar conteúdo e propriedades** | Sim                                | Não                                              |
| **Multilingue**               | Sim                                | Não                                              |
| **Emitir links**                 | Sim                                | Não                                              |
| **MIME**                       | Sim                                | Não                                              |
| **Limites de texto**            | Frase, parágrafo, capítulo       | Nenhum                                            |
| **Cliente/servidor**            | Ambos                               | Cliente                                          |
| **Implementação**             | Complex                            | Simples                                          |

**Manipuladores de propriedades**  Manipuladores de propriedades são componentes que leem e escrevem propriedades para um formato de arquivo específico. Eles acessam itens e emitem propriedades para o coletor da mesma maneira que os filtros fazem para o conteúdo. Os manipuladores de propriedades são mais fáceis de implementar do que os filtros. Se um formato de arquivo baseado em texto for muito simples ou os arquivos devem ser muito pequenos, o manipulador de propriedades poderá emitir propriedades e conteúdo.

> [!NOTE]  
> Os manipuladores de propriedades não são Windows Search componentes; eles são componentes relacionados ao formato de arquivo específico que foram projetados para acessar. Para obter mais informações sobre manipuladores de propriedades e como implementar um para um formato de arquivo personalizado, consulte [Desenvolvendo](-search-3x-wds-extidx-propertyhandlers.md)manipuladores de propriedades para Windows Search .

**Propriedades** Windows Search fornece um [sistema de propriedades](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) que inclui uma grande biblioteca de propriedades. Qualquer propriedade pode aparecer em qualquer item, conforme definido pelo filtro ou manipulador de propriedades. Se você tiver um formato de arquivo personalizado, poderá mapear as propriedades do formato de arquivo para essas propriedades do sistema e criar novas propriedades personalizadas. Quando o manipulador de propriedades ou filtro emite essas propriedades, o coletor atualiza o índice para que os usuários possam pesquisar usando suas propriedades. Para obter mais informações sobre como criar e registrar propriedades personalizadas para um formato de arquivo, consulte [Sistema de propriedades](../properties/building-property-handlers.md).

**SystemIndex**  O índice, chamado SystemIndex, armazena dados indexados e é composto por um armazenamento de propriedades e índices sobre as propriedades e o conteúdo das propriedades do item e um índice invertido para conteúdo textual e propriedades. Depois que o coletor atualiza o índice, o índice pode ser consultado por Windows Search e outros aplicativos. Para obter mais informações sobre maneiras de consultar o índice, consulte [Consultando o índice programaticamente.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Lembre-se de que, quando você registra um esquema de novo, as alterações feitas em atributos de propriedades definidas anteriormente podem não ser respeitadas pelo indexador. A solução é recriar o índice ou introduzir novas propriedades que refletem as alterações em vez de atualizar as antigas (não recomendadas). Para obter mais informações, consulte [Observação para implementadores em](#notes-to-implementers) Visão geral do sistema de [propriedades](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Como a indexação é agendada

Quando Windows Search é instalado pela primeira vez, ele executa uma indexação completa do escopo de rastreamento, pausando durante períodos de alta E/S e atividade do usuário. O escopo de rastreamento padrão consiste nos locais de biblioteca padrão, como **Documentos,** **Música,** **Imagens** e **Vídeos.** As notificações são processadas mesmo antes que o rastreamento inicial seja concluído. Ocasionalmente, o coletor rastrea as URLs do escopo de rastreamento completo. Esses rastreamentos completos garantem que os dados no índice estão atualizados. Por exemplo, se um provedor de notificação não enviar notificações ou se o serviço Windows Search for encerrado inesperadamente, o coletor não terá conhecimento de itens novos ou alterados e não indexará esses itens. Há dois tipos de fontes: somente notificação e notificação habilitada. Em ambas as fontes, o coletor rastrea inicialmente o índice. Após o rastreamento inicial, as fontes somente notificação nunca fazerão um rastreamento completo novamente, a menos que haja uma falha, como a rolagem do Diário de Alterações da [USN.](/windows/desktop/FileIO/change-journals) As fontes habilitadas para notificação fazem um rastreamento incremental quando o indexador é iniciado, mas escutam as notificações durante a execução. NTFS e Microsoft Outlook são apenas notificação. Internet Explorer e FAT estão habilitados para notificação.

## <a name="notes-to-implementers"></a>Notas aos Implementadores

A qualidade dos dados no índice e a eficiência do processo de indexação dependem muito da implementação do filtro e do manipulador de propriedades. Como o filtro é chamado sempre que uma URL identifica o formato de arquivo, o processo de indexação pode diminuir drasticamente se o filtro for ineficiente. Se o manipulador de propriedades não mapear corretamente todas as propriedades de arquivo para as propriedades do sistema ou não emitir corretamente essas propriedades, os dados no índice estarão incorretos e pesquisas posteriores para essas propriedades retornarão resultados incorretos. Se o filtro ou o manipulador de propriedades falhar, o indexador não poderá indexar dados.

Aplicativos e processos diferentes Windows Search dependem de manipuladores de protocolo, filtros e manipuladores de propriedade. Suas implementações podem afetar esses aplicativos de maneiras que talvez você não espere. O [guia Windows Search desenvolvimento do](-search-developers-guide-entry-page.md) Windows Search fornece conselhos sobre opções de design e sobre como testar cada um desses componentes.

## <a name="related-topics"></a>Tópicos relacionados

[Indexação, consulta e notificações em Windows Search](-search-3x-wds-included-in-index.md)

[O que está incluído no índice](-search-indexing-process-overview.md)

[Processo de consulta em Windows Search](querying-process--windows-search-.md)

[Processo de notificações em Windows Search](-search-3x-wds-support.md)

[Requisitos de formatação de URL](url-formatting-requirements.md)
