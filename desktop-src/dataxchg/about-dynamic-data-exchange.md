---
title: Sobre troca dinâmica de dados
description: Este tópico discute a transferência de dados entre aplicativos.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- Troca dinâmica de dados (DDE), sobre
- DDE (troca dinâmica de dados), sobre
- troca de dados, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), vinculando a dados em tempo real
- DDE (troca dinâmica de dados), vinculando a dados em tempo real
- Troca dinâmica de dados (DDE), criando documentos compostos
- DDE (troca dinâmica de dados), criando documentos compostos
- Troca dinâmica de dados (DDE), consultas de dados
- DDE (troca dinâmica de dados), consultas de dados
- Troca dinâmica de dados (DDE), exemplos
- DDE (troca dinâmica de dados), exemplos
- Troca dinâmica de dados (DDE), representação
- DDE (troca dinâmica de dados), representação
- Troca dinâmica de dados (DDE), mensagens
- DDE (troca dinâmica de dados), mensagens
- Troca dinâmica de dados (DDE), Atoms
- DDE (troca dinâmica de dados), Atoms
- Troca dinâmica de dados (DDE), objetos de memória compartilhada
- DDE (troca dinâmica de dados), objetos de memória compartilhada
- Troca dinâmica de dados (DDE), funções de empacotamento de parâmetro
- DDE (troca dinâmica de dados), funções de empacotamento de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366513"
---
# <a name="about-dynamic-data-exchange"></a>Sobre troca dinâmica de dados

O Windows fornece vários métodos para transferir dados entre aplicativos. Um método é usar o protocolo troca dinâmica de dados (DDE). O protocolo DDE é um conjunto de mensagens e diretrizes. Ele envia mensagens entre aplicativos que compartilham dados e usa a memória compartilhada para trocar dados entre aplicativos. Os aplicativos podem usar o protocolo DDE para transferências de dados one-time e para trocas contínuas nas quais os aplicativos enviam atualizações entre si à medida que novos dados ficam disponíveis.

O Windows também dá suporte à DDEML (biblioteca de gerenciamento de troca dinâmica de dados). O DDEML é uma DLL (biblioteca de vínculo dinâmico) que os aplicativos podem usar para compartilhar dados. O DDEML fornece funções e mensagens que simplificam a tarefa de adicionar capacidade DDE a um aplicativo. Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções de DDEML para gerenciar conversas DDE. (Uma conversa DDE é a interação entre aplicativos cliente e servidor.)

O DDEML também fornece um recurso para gerenciar as cadeias de caracteres e os dados que os aplicativos DDE compartilham. Em vez de usar Atoms e ponteiros para objetos de memória compartilhados, os aplicativos DDE criam e trocam identificadores de cadeias de caracteres, que identificam cadeias e identificadores de dados, que identificam objetos de memória. O DDEML também possibilita que um aplicativo de servidor registre os nomes de serviço com suporte. Os nomes são transmitidos para outros aplicativos no sistema, que podem usar os nomes para se conectar ao servidor. Além disso, o DDEML garante a compatibilidade entre aplicativos DDE, forçando-os a implementar o protocolo DDE de maneira consistente.

Os aplicativos existentes que usam o protocolo DDE baseado em mensagem são totalmente compatíveis com aqueles que usam o DDEML. Ou seja, um aplicativo que usa o DDE baseado em mensagem pode estabelecer conversas e executar transações com aplicativos que usam o DDEML. Devido às muitas vantagens do DDEML, os novos aplicativos devem usá-lo em vez de mensagens DDE. Para usar os elementos de API do DDEML, você deve incluir o arquivo de cabeçalho DDEML em seus arquivos de origem, vincular com a biblioteca DDEML e garantir que a biblioteca de vínculo dinâmico de DDEML esteja no caminho de pesquisa do sistema.

Os tópicos a seguir são discutidos nesta seção.

-   [Protocolo troca dinâmica de dados](#dynamic-data-exchange-protocol)
-   [Usos do para Windows troca dinâmica de dados](#uses-for-windows-dynamic-data-exchange)
-   [troca dinâmica de dados do ponto de vista do usuário](#dynamic-data-exchange-from-the-users-point-of-view)
-   [Conceitos de troca dinâmica de dados](#dynamic-data-exchange-concepts)
    -   [Cliente, servidor e conversa](#client-server-and-conversation)
    -   [Nomes de aplicativo, tópico e item](#application-topic-and-item-names)
    -   [O tópico System](#the-system-topic)
    -   [Links de dados permanentes](#permanent-data-links)
    -   [Atoms e objetos de memória compartilhada](#atoms-and-shared-memory-objects)
-   [Visão geral de mensagens de troca dinâmica de dados](#dynamic-data-exchange-messages-overview)
-   [Fluxo de mensagens troca dinâmica de dados](#dynamic-data-exchange-message-flow)
-   [Funções de empacotamento de parâmetro](#parameter-packing-functions)
-   [troca dinâmica de dados e representação](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>Protocolo troca dinâmica de dados

Como o Windows tem uma arquitetura baseada em mensagens, a passagem de mensagens é o método mais apropriado para transferir automaticamente as informações entre os aplicativos. No entanto, as mensagens contêm apenas dois parâmetros (*wParam* e *lParam*) para a passagem de dados. Como resultado, esses parâmetros devem se referir indiretamente a outras partes de dados quando mais de algumas palavras de informações forem passadas entre os aplicativos. O protocolo DDE define exatamente como os aplicativos devem usar os parâmetros *wParam* e *lParam* para passar grandes partes de dados por meio de átomos globais e identificadores de memória compartilhada. O protocolo DDE tem regras específicas para alocar e excluir Atoms globais e objetos de memória compartilhados.

Um Atom global é uma referência a uma cadeia de caracteres. No protocolo DDE, os Atoms identificam os aplicativos que trocam dados, a natureza dos dados que estão sendo trocados e os próprios itens de dados. Para obter mais informações sobre Atoms, consulte [sobre Atoms](about-atom-tables.md).

## <a name="uses-for-windows-dynamic-data-exchange"></a>Usos do para Windows troca dinâmica de dados

O DDE é mais apropriado para trocas de dados que não exigem interação contínua do usuário. Normalmente, um aplicativo fornece um método para que o usuário estabeleça o vínculo entre os aplicativos trocando dados. Quando esse link é estabelecido, no entanto, os aplicativos trocam dados sem o envolvimento adicional do usuário.

O DDE pode ser usado para implementar uma ampla gama de recursos de aplicativos, por exemplo:

-   Vinculação a dados em tempo real, como atualizações de mercado de ações, instrumentos científicos ou controle de processo.
-   Criar documentos compostos, como um documento de processamento de texto que inclui um gráfico produzido por um aplicativo gráfico. Usando o DDE, o gráfico será alterado quando os dados de origem forem alterados, enquanto o restante do documento permanecerá o mesmo.
-   Executar consultas de dados entre aplicativos, como uma planilha consultando um banco de dado para contas vencidas.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>troca dinâmica de dados do ponto de vista do usuário

O exemplo a seguir ilustra como dois aplicativos DDE podem cooperar, como visto no ponto de vista do usuário.

Um usuário de planilha deseja usar o Microsoft Excel para controlar o preço de um estoque específico na bolsa de ações de Nova York. O usuário tem um aplicativo chamado quote que, por sua vez, tem acesso aos dados do NYSE. A conversa DDE entre o Excel e as cotações ocorre da seguinte maneira:

-   O usuário inicia a conversa fornecendo o nome do aplicativo (cotação) que fornecerá os dados e o tópico específico de interesse (NYSE). A conversa DDE resultante é usada para solicitar aspas em ações específicas.
-   O Excel transmite os nomes do aplicativo e do tópico para todos os aplicativos DDE atualmente em execução no sistema. A cotação responde, estabelecendo uma conversa com o Excel sobre o tópico da NYSE.
-   Em seguida, o usuário pode criar uma fórmula de planilha em uma célula que solicita que a planilha seja atualizada automaticamente sempre que uma determinada cotação de ações for alterada. Por exemplo, o usuário pode solicitar uma atualização automática sempre que uma alteração ocorrer no preço de venda de ZAXX Stock especificando a seguinte fórmula do Excel: = ' quote ' \| ' NYSE '! ZAXX
-   O usuário pode encerrar a atualização automática da cotação de ações do ZAXX a qualquer momento. Outros links de dados que foram estabelecidos separadamente (como para Cotações para outras ações) ainda permanecerão ativos na mesma conversa da NYSE.
-   O usuário também pode encerrar toda a conversa entre o Excel e as aspas no tópico da NYSE, para que não seja possível estabelecer links de dados específicos sobre esse tópico sem iniciar uma nova conversa.

## <a name="dynamic-data-exchange-concepts"></a>Conceitos de troca dinâmica de dados

As seções a seguir explicam os conceitos e a terminologia importantes que são fundamentais para compreender o intercâmbio dinâmico de dados.

-   [Cliente, servidor e conversa](#client-server-and-conversation)
-   [Nomes de aplicativo, tópico e item](#application-topic-and-item-names)
-   [O tópico System](#the-system-topic)
-   [Links de dados permanentes](#permanent-data-links)
-   [Atoms e objetos de memória compartilhada](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Cliente, servidor e conversa

Dois aplicativos que participam do DDE são considerados envolvidos em uma conversa DDE. O aplicativo que inicia a conversa é o aplicativo cliente DDE; o aplicativo que responde ao cliente é o aplicativo do servidor DDE. Um aplicativo pode envolver várias conversas ao mesmo tempo, agindo como o cliente em algum e como o servidor em outros.

Uma conversa DDE ocorre entre duas janelas, uma para cada um dos aplicativos participantes. Uma janela pode ser a janela principal do aplicativo; uma janela associada a um documento específico, como em um aplicativo de interface de vários documentos (MDI); ou uma janela oculta (invisível) cuja única finalidade é processar mensagens DDE.

Como uma conversa DDE é identificada pelo par de identificadores para as janelas envolvidas na conversa, nenhuma janela deve ser envolvida em mais de uma conversa com outra janela. O aplicativo cliente ou o aplicativo de servidor deve fornecer uma janela diferente para cada uma de suas conversas com um aplicativo cliente ou servidor específico.

Um aplicativo pode garantir que um par de clientes e janelas de servidor nunca esteja envolvido em mais de uma conversa criando uma janela oculta para cada conversa. A única finalidade desta janela é processar mensagens DDE.

### <a name="application-topic-and-item-names"></a>Nomes de aplicativo, tópico e item

O protocolo DDE identifica as unidades de dados passadas entre o cliente e o servidor com uma hierarquia de três níveis de nomes de aplicativo, de tópico e de item.

Cada conversa DDE é definida exclusivamente pelo nome do aplicativo e pelo tópico. No início de uma conversa DDE, o cliente e o servidor determinam o nome e o tópico do aplicativo. O nome do aplicativo geralmente é o nome do aplicativo do servidor. Por exemplo, quando o Excel atua como o servidor em uma conversa, o nome do aplicativo é Excel.

O tópico DDE é uma classificação geral dos dados dentro dos quais vários itens de dados podem ser "discutidos" (trocados) durante a conversa. Para aplicativos que operam em documentos baseados em arquivo, o tópico geralmente é um nome de arquivo. Para outros aplicativos, o tópico é um nome específico do aplicativo.

Como a janela cliente e servidor lida em conjunto, identifique uma conversa DDE, o nome do aplicativo e o tópico que definem uma conversa não podem ser alterados durante o curso da conversa.

Um item de dados DDE é uma informação relacionada ao tópico de conversa trocado entre os aplicativos. Os valores para o item de dados podem ser passados do servidor para o cliente ou do cliente para o servidor. Os dados podem ser passados com qualquer um dos formatos de área de transferência padrão ou com um formato de área de transferência registrado. Um formato de nome registrado e especial chamado link identifica um item em uma conversa DDE. Para obter mais informações sobre formatos de área de transferência, consulte [área de transferência](clipboard.md).

### <a name="the-system-topic"></a>O tópico System

Os aplicativos devem dar suporte ao tópico do sistema em todos os momentos. Este tópico fornece um contexto para informações que podem ser de interesse geral para outro aplicativo.

Os valores de item de dados devem ser renderizados no formato de área de transferência de [**\_ texto do CF**](standard-clipboard-formats.md) . Elementos individuais de valores de item para um tópico do sistema devem ser delimitados por caracteres de tabulação. A tabela a seguir sugere alguns itens para o tópico System.



| Item          | Descrição                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formatos       | Lista delimitada por tabulação de formatos de área de transferência que o aplicativo pode renderizar. Normalmente, os formatos de **CF \_** são listados com a parte "**CF \_**" dos nomes removidos (por exemplo, o **\_ texto de CF** é listado como "**texto**").                                                                                        |
| Ajuda          | Texto que explica brevemente como usar o servidor DDE.                                                                                                                                                                                                                                                   |
| ReturnMessage | Detalhes de suporte para a mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) usada mais recentemente. Esse item é útil quando mais de oito bits de dados de retorno específicos do aplicativo são necessários.                                                                                                                |
| Status        | Indicação do status atual do aplicativo. Quando um servidor recebe uma mensagem de [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) para este item de tópico do sistema, ele deve responder postando uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) com uma cadeia de caracteres que contenha ocupado ou pronto, conforme apropriado. |
| SysItems      | Lista de itens de tópico do sistema para os quais o aplicativo dá suporte.                                                                                                                                                                                                                                                    |
| TopicItemList | Semelhante ao item SysItems, exceto que TopicItemList deve ter suporte para cada tópico que não seja o tópico System. Isso permite a navegação dos itens com suporte em qualquer tópico. Se os itens não puderem ser enumerados, esse item deverá conter apenas "TopicItemList".                                  |
| Tópicos        | Lista de tópicos aos quais o aplicativo dá suporte no momento atual; Essa lista pode variar desde o momento até o momento.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Links de dados permanentes

Depois que uma conversa DDE é iniciada, o cliente pode estabelecer um ou mais links de dados permanentes com o servidor. Um link de dados é um mecanismo de comunicações pelo qual o servidor notifica o cliente sempre que o valor de um item de dados especificado é alterado. O link de dados é permanente no sentido de que esse processo de notificação continua até que o link de dados ou a própria conversa DDE seja encerrada.

Há dois tipos de vínculos de dados DDE permanentes: quente e quente. Em um link de dados quentes, o servidor notifica o cliente de que o valor do item de dados foi alterado, mas o servidor não envia o valor de dados para o cliente até que o cliente o solicite. Em um link de dados dinâmicos, o servidor envia imediatamente o valor de dados alterado para o cliente.

Os aplicativos que dão suporte a links de dados quentes ou Hot data normalmente fornecem um comando **copiar** ou **colar link** no menu **Editar** para permitir que o usuário estabeleça links entre aplicativos.

### <a name="atoms-and-shared-memory-objects"></a>Atoms e objetos de memória compartilhada

Determinados argumentos de mensagens DDE são Atoms globais ou objetos de memória compartilhada. Os aplicativos que usam esses argumentos devem seguir regras explícitas sobre quando alocar e excluí-los. Em todos os casos, o remetente da mensagem deve excluir qualquer objeto Atom ou de memória compartilhada que o receptor pretendido não receberá por causa de uma condição de erro, como falha da função de [**mensagem**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

O DDE usa objetos de memória compartilhada para três finalidades:

-   Para transportar um valor de item de dados a ser trocado. Este é um item referenciado pelo parâmetro *hData* nos [**dados do \_ WM \_ DDE**](wm-dde-data.md) e no [**WM DDE enmediate \_ \_**](wm-dde-poke.md) messages.
-   Para transportar opções em uma mensagem. Este é um item referenciado pelo parâmetro *hOptions* em uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) .
-   Para executar uma cadeia de caracteres de execução de comando. Este é um item referenciado pelo parâmetro *hCommands* na mensagem [**de \_ \_ execução de DDE do WM**](wm-dde-execute.md) e sua mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) correspondente.

Um aplicativo que recebe um objeto de memória compartilhada DDE deve tratá-lo como somente leitura. O aplicativo não deve usar o objeto como uma área de leitura/gravação mútua para a troca de dados gratuita.

Como acontece com um átomo DDE, um aplicativo deve liberar um objeto de memória compartilhada para gerenciar a memória com eficiência. O aplicativo também deve bloquear e desbloquear os objetos de memória.

## <a name="dynamic-data-exchange-messages-overview"></a>Visão geral de mensagens de troca dinâmica de dados

Como o DDE é um protocolo baseado em mensagem, ele emprega nenhuma função ou biblioteca. Todas as transações DDE são realizadas passando determinadas mensagens DDE definidas entre as janelas do cliente e do servidor.

Há nove mensagens DDE; as constantes simbólicas para essas mensagens são definidas no arquivo de cabeçalho DDE. Determinadas estruturas para as várias mensagens DDE também são definidas neste arquivo de cabeçalho.

A tabela a seguir resume as mensagens DDE.



| Mensagem                                        | Descrição                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK de DDE do WM \_**](wm-dde-ack.md)             | Confirma o recebimento ou não do recebimento de uma mensagem.                                                                                               |
| [**\_aviso de DDE do WM \_**](wm-dde-advise.md)       | Solicita que o aplicativo de servidor forneça uma atualização ou notificação para um item de dados sempre que ele for alterado. Isso estabelece um link de dados permanente. |
| [**\_dados DDE do WM \_**](wm-dde-data.md)           | Envia um valor de item de dados para o aplicativo cliente.                                                                                               |
| [**\_execução de DDE do WM \_**](wm-dde-execute.md)     | Envia uma cadeia de caracteres para o aplicativo de servidor, que deve processar a cadeia de caracteres como uma série de comandos.                                       |
| [**início do WM \_ DDE \_**](wm-dde-initiate.md)   | Inicia uma conversa entre os aplicativos cliente e servidor.                                                                             |
| [**o WM \_ DDE. \_**](wm-dde-poke.md)           | Envia um valor de item de dados para o aplicativo de servidor.                                                                                               |
| [**\_solicitação de DDE do WM \_**](wm-dde-request.md)     | Solicita que o aplicativo de servidor forneça o valor de um item de dados.                                                                             |
| [**fim do WM \_ DDE \_**](wm-dde-terminate.md) | Encerra uma conversa.                                                                                                                       |
| [**\_aviso de DDE do WM \_**](wm-dde-unadvise.md)   | Encerra um link de dados permanente.                                                                                                                |



 

Um aplicativo chama [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para emitir a mensagem de [**\_ \_ início do WM DDE**](wm-dde-initiate.md) ou uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) enviada em resposta a **início do WM \_ DDE \_**. Todas as outras mensagens são enviadas por uma [**mensagem**](/windows/desktop/api/winuser/nf-winuser-postmessagea). O primeiro parâmetro dessas chamadas é um identificador para a janela de recebimento; o segundo parâmetro contém a mensagem a ser enviada; o terceiro parâmetro identifica a janela de envio; e o quarto parâmetro contém os argumentos específicos da mensagem.

## <a name="dynamic-data-exchange-message-flow"></a>Fluxo de mensagens troca dinâmica de dados

Uma conversa DDE típica consiste nos seguintes eventos:

1.  O aplicativo cliente inicia a conversa e o aplicativo do servidor responde.
2.  Os aplicativos trocam dados por um ou todos os seguintes métodos:
    -   -   O aplicativo de servidor envia dados para o cliente na solicitação do cliente.
        -   O aplicativo cliente envia dados não solicitados para o aplicativo de servidor.
        -   O aplicativo cliente solicita que o aplicativo de servidor notifique o cliente sempre que um item de dados for alterado (link de dados quentes).
        -   O aplicativo cliente solicita que o aplicativo de servidor envie dados sempre que os dados forem alterados (link de dados dinâmicos).
        -   O aplicativo de servidor executa um comando na solicitação do cliente.

3.  O aplicativo cliente ou servidor encerra a conversa.

Uma janela de aplicativo que processa solicitações de um cliente ou servidor deve processá-las estritamente na ordem em que são recebidas.

Um cliente pode estabelecer conversas com mais de um servidor; um servidor pode ter conversas com mais de um cliente. Ao lidar com mensagens de mais de uma fonte, um cliente ou servidor deve processar as mensagens de uma conversa de forma síncrona, mas não precisa processar todas as mensagens de forma síncrona. Em outras palavras, ele pode mudar de uma conversa para outra, conforme necessário.

Se um aplicativo não puder processar uma solicitação de entrada porque está aguardando uma resposta DDE, ele deverá impedir o deadlock postando uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) com o membro **fBusy** da estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) definida como 1. Um aplicativo também pode enviar uma mensagem **de \_ \_ ACK DDE** ocupada do WM se, por algum motivo, ele não puder processar uma solicitação de entrada dentro de um período de tempo razoável.

Um aplicativo deve ser capaz de lidar com a falha de um cliente ou servidor para responder a uma mensagem dentro de um determinado tempo. Como o intervalo de tempo limite pode variar dependendo da natureza do aplicativo e da configuração do sistema do usuário (incluindo se ele está conectado a uma rede), o aplicativo deve fornecer uma maneira para o usuário especificar o intervalo.

## <a name="parameter-packing-functions"></a>Funções de empacotamento de parâmetro

O parâmetro *lParam* de muitas mensagens DDE contém duas partes de dados. Por exemplo, o *lParam* da mensagem [**de \_ \_ dados DDE do WM**](wm-dde-data.md) contém um identificador de dados e um Atom. Os aplicativos devem usar a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) para empacotar o identificador e o Atom em um parâmetro *lParam* e a função [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para remover os valores. Os aplicativos DDE devem usar **PackDDElParam** e **UnpackDDElParam** para todas as mensagens lançadas durante uma conversa DDE.

Os aplicativos também podem usar as funções [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) e [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) . O **ReuseDDElParam** permite que um aplicativo DDE reutilize um parâmetro *lParam* embalado, ajudando a reduzir o número de realocações de memória que o aplicativo deve executar durante uma conversa. Um aplicativo pode usar **FreeDDElParam** para liberar a memória associada a um identificador de dados recebido durante uma conversa DDE.

## <a name="dynamic-data-exchange-and-impersonation"></a>troca dinâmica de dados e representação

Para permitir que um servidor represente um cliente, o cliente chama a função [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) . A estrutura do [**\_ \_ nível de representação de segurança**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) é usada para controlar o nível de representação que o servidor pode executar.

Um servidor DDE pode representar um cliente DDE chamando a função [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) . Um servidor DDEML deve usar a função [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) .

 

 