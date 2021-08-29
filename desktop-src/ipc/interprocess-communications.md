---
description: o sistema operacional Windows fornece mecanismos para facilitar a comunicação e o compartilhamento de dados entre aplicativos. Coletivamente, as atividades habilitadas por esses mecanismos são chamadas de IPC (comunicações entre processos).
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Comunicação entre processos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5632443187ba9e50ed6c7f1adb31e8a02a280735c99dd8ee5455d2f067ef263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756315"
---
# <a name="interprocess-communications"></a>Comunicação entre processos

o sistema operacional Windows fornece mecanismos para facilitar a comunicação e o compartilhamento de dados entre aplicativos. Coletivamente, as atividades habilitadas por esses mecanismos são chamadas de IPC ( *comunicações entre processos* ). Algumas formas de IPC facilitam a divisão de trabalho entre vários processos especializados. Outras formas de IPC facilitam a divisão de trabalho entre computadores em uma rede.

Normalmente, os aplicativos podem usar o IPC Categorizado como clientes ou servidores. Um *cliente* é um aplicativo ou um processo que solicita um serviço de algum outro aplicativo ou processo. Um *servidor* é um aplicativo ou um processo que responde a uma solicitação do cliente. Muitos aplicativos atuam como um cliente e um servidor, dependendo da situação. Por exemplo, um aplicativo de processamento de texto pode atuar como um cliente ao solicitar uma tabela de Resumo de custos de produção de um aplicativo de planilha atuando como um servidor. O aplicativo de planilha, por sua vez, pode atuar como um cliente na solicitação dos níveis de inventário mais recentes de um aplicativo de controle de inventário automatizado.

Depois de decidir que seu aplicativo se beneficiaria do IPC, você deve decidir quais dos métodos IPC disponíveis usar. É provável que um aplicativo use vários mecanismos de IPC. As respostas a essas perguntas determinam se um aplicativo pode se beneficiar usando um ou mais mecanismos IPC.

-   O aplicativo deve ser capaz de se comunicar com outros aplicativos em execução em outros computadores em uma rede ou é suficiente para que o aplicativo se comunique apenas com os aplicativos no computador local?
-   o aplicativo deve ser capaz de se comunicar com aplicativos em execução em outros computadores que possam estar sendo executados em sistemas operacionais diferentes (como Windows de 16 bits ou UNIX)?
-   O usuário do aplicativo deve escolher os outros aplicativos com os quais o aplicativo se comunica, ou o aplicativo pode encontrar implicitamente seus parceiros cooperativos?
-   O aplicativo deve se comunicar com vários aplicativos diferentes de forma geral, como permitir operações de recortar e colar com qualquer outro aplicativo, ou os requisitos de comunicação devem ser limitados a um conjunto restrito de interações com outros aplicativos específicos?
-   O desempenho é um aspecto crítico do aplicativo? Todos os mecanismos de IPC incluem alguma quantidade de sobrecarga.
-   O aplicativo deve ser um aplicativo de GUI ou um aplicativo de console? Alguns mecanismos de IPC exigem um aplicativo de GUI.

Os mecanismos de IPC a seguir têm suporte pelo Windows:

-   [Área de transferência](#using-the-clipboard-for-ipc)
-   [INTERFACES](#using-com-for-ipc)
-   [Cópia de dados](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Mapeamento de arquivo](#using-a-file-mapping-for-ipc)
-   [Processadores](#using-a-mailslot-for-ipc)
-   [Pipes](#using-pipes-for-ipc)
-   [RPC](#using-rpc-for-ipc)
-   [Windows Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Usando a área de transferência para IPC

A área de transferência atua como um depósito central para o compartilhamento de dados entre aplicativos. Quando um usuário executa uma operação de recortar ou copiar em um aplicativo, o aplicativo coloca os dados selecionados na área de transferência em um ou mais formatos padrão ou definidos pelo aplicativo. Qualquer outro aplicativo pode recuperar os dados da área de transferência, escolhendo os formatos disponíveis que ele compreende. A área de transferência é um meio de troca muito menos flexível, em que os aplicativos precisam apenas concordar com o formato dos dados. Os aplicativos podem residir no mesmo computador ou em computadores diferentes em uma rede.

**Ponto-chave:** Todos os aplicativos devem dar suporte à área de transferência para os formatos de dados que eles entendem. Por exemplo, um editor de texto ou processador de textos deve, pelo menos, ser capaz de produzir e aceitar dados da área de transferência em formato de texto puro. Para obter mais informações, consulte [área de transferência](../dataxchg/clipboard.md).

## <a name="using-com-for-ipc"></a>Usando COM para IPC

Os aplicativos que usam OLE gerenciam *documentos compostos*, ou seja, documentos compostos de dados de uma variedade de aplicativos diferentes. O OLE fornece serviços que facilitam a chamada de aplicativos em outros aplicativos para a edição de dados. Por exemplo, um processador de texto que usa OLE pode inserir um grafo de uma planilha. O usuário pode iniciar a planilha automaticamente de dentro do processador de texto escolhendo o gráfico incorporado para edição. O OLE cuida da inicialização da planilha e da apresentação do grafo para edição. Quando o usuário sai da planilha, o grafo seria atualizado no documento original do processador de texto. A planilha parece ser uma extensão do processador de texto.

A base do OLE é a Component Object Model (COM). Um componente de software que usa o COM pode se comunicar com uma ampla variedade de outros componentes, até mesmo aqueles que ainda não foram escritos. Os componentes interagem como objetos e clientes. Distributed COM estende o modelo de programação COM para que ele funcione em uma rede.

**Ponto-chave:** O OLE dá suporte a documentos compostos e permite que um aplicativo inclua dados inseridos ou vinculados que, quando escolhido, inicie automaticamente outro aplicativo para edição de dados. Isso permite que o aplicativo seja estendido por qualquer outro aplicativo que usa OLE. Os objetos COM fornecem acesso aos dados de um objeto por meio de um ou mais conjuntos de funções relacionadas, conhecidos como *interfaces*. para obter mais informações, consulte COM e ActiveX Serviços de Objeto.

## <a name="using-data-copy-for-ipc"></a>Usando cópia de dados para IPC

A cópia de dados permite que um aplicativo envie informações para outro aplicativo usando a mensagem [**\_ CopyData do WM**](../dataxchg/wm-copydata.md) . Esse método requer a cooperação entre o aplicativo de envio e o aplicativo de recebimento. O aplicativo de recebimento deve saber o formato das informações e ser capaz de identificar o remetente. O aplicativo de envio não pode modificar a memória referenciada por nenhum ponteiro.

**Ponto-chave:** a cópia de dados pode ser usada para enviar informações rapidamente para outro aplicativo usando Windows mensagens. Para obter mais informações, consulte [cópia de dados](../dataxchg/data-copy.md).

## <a name="using-dde-for-ipc"></a>Usando o DDE para IPC

O DDE é um protocolo que permite que os aplicativos troquem dados em uma variedade de formatos. Os aplicativos podem usar o DDE para trocas de dados de uso único ou para trocas contínuas nas quais os aplicativos se atualizam um ao outro à medida que novos dados se tornam disponíveis.

Os formatos de dados usados pelo DDE são os mesmos usados pela área de transferência. O DDE pode ser considerado uma extensão do mecanismo da área de transferência. A área de transferência é quase sempre usada para uma resposta única para um comando de usuário, como escolher o comando colar em um menu. O DDE também é normalmente iniciado por um comando de usuário, mas geralmente continua a funcionar sem interação adicional do usuário. Você também pode definir formatos de dados DDE personalizados para IPC de propósito especial entre aplicativos com requisitos de comunicação mais rigidamente acoplados.

As trocas DDE podem ocorrer entre aplicativos em execução no mesmo computador ou em computadores diferentes em uma rede.

**Ponto-chave:** O DDE não é tão eficiente quanto as tecnologias mais recentes. No entanto, você ainda poderá usar o DDE se outros mecanismos de IPC não forem adequados ou se você precisar interagir com um aplicativo existente que dá suporte apenas a DDE. para obter mais informações, consulte [troca dinâmica de dados](../dataxchg/dynamic-data-exchange.md) e [troca dinâmica de dados biblioteca de gerenciamento](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Usando um mapeamento de arquivo para IPC

O *mapeamento de arquivo* permite que um processo trate o conteúdo de um arquivo como se fosse um bloco de memória no espaço de endereço do processo. O processo pode usar operações de ponteiro simples para examinar e modificar o conteúdo do arquivo. Quando dois ou mais processos acessam o mesmo mapeamento de arquivo, cada processo recebe um ponteiro para a memória em seu próprio espaço de endereço que pode ser usado para ler ou modificar o conteúdo do arquivo. Os processos devem usar um objeto de sincronização, como um semáforo, para evitar corrupção de dados em um ambiente multitarefa.

Você pode usar um caso especial de mapeamento de arquivo para fornecer *memória compartilhada nomeada* entre processos. Se você especificar o arquivo de permuta do sistema ao criar um objeto de mapeamento de arquivo, o objeto de mapeamento de arquivo será tratado como um bloco de memória compartilhada. Outros processos podem acessar o mesmo bloco de memória abrindo o mesmo objeto de mapeamento de arquivo.

O mapeamento de arquivo é bastante eficiente e também fornece atributos de segurança com suporte do sistema operacional que podem ajudar a evitar corrupção de dados não autorizados. O mapeamento de arquivo pode ser usado somente entre processos em um computador local; Ele não pode ser usado em uma rede.

**Ponto-chave:** O mapeamento de arquivo é uma maneira eficiente para dois ou mais processos no mesmo computador compartilharem dados, mas você deve fornecer sincronização entre os processos. Para obter mais informações, consulte [mapeamento de arquivo](/windows/desktop/Memory/file-mapping) e [sincronização](/windows/desktop/Sync/synchronization).

## <a name="using-a-mailslot-for-ipc"></a>Usando um processador de processadores para IPC

Os processadores fornecem uma comunicação unidirecional. Qualquer processo que cria um processador de processadores é um *servidor de processador de processadores*. Outros processos, chamados de *clientes do processador*, enviam mensagens para o servidor do processador de mensagens gravando uma mensagem em seu processador. As mensagens de entrada são sempre acrescentadas ao processador. A mala postal salva as mensagens até que o servidor do processador de mensagens as Leia. Um processo pode ser um servidor de processador de processadores e um cliente de processador de processadores, portanto, a comunicação bidirecional é possível usando vários processadores de processamento.

Um cliente do processador de mensagens pode enviar uma mensagem para um processador de processadores no computador local, para um processador de processadores em outro computador ou para todos os processadores de mensagens com o mesmo nome em todos os computadores em um domínio de rede especificado. As mensagens transmitidas para todos os processadores de bytes em um domínio não podem ter mais de 400 MB, enquanto as mensagens enviadas a um único processador são limitadas apenas pelo tamanho máximo da mensagem especificado pelo servidor do processador de mensagens quando ele criou o processador de bytes.

**Ponto-chave:** Os processadores de mensagens oferecem uma maneira fácil para que os aplicativos enviem e recebam mensagem curta. Eles também fornecem a capacidade de transmitir mensagens entre todos os computadores em um domínio de rede. Para obter mais informações, consulte [processadores](mailslots.md)de enup.

## <a name="using-pipes-for-ipc"></a>Usando pipes para IPC

Há dois tipos de pipes para comunicação bidirecional: Pipes anônimos e pipes nomeados. Os *Pipes anônimos* permitem que os processos relacionados transfiram informações entre si. Normalmente, um pipe anônimo é usado para redirecionar a entrada ou saída padrão de um processo filho para que ele possa trocar dados com seu processo pai. Para trocar dados em ambas as direções (operação duplex), você deve criar dois pipes anônimos. O processo pai grava dados em um pipe usando seu identificador de gravação, enquanto o processo filho lê os dados desse pipe usando seu identificador de leitura. Da mesma forma, o processo filho grava dados no outro pipe e o processo pai lê dele. Pipes anônimos não podem ser usados em uma rede nem podem ser usados entre processos não relacionados.

*Pipes nomeados* são usados para transferir dados entre processos que não são processos relacionados e entre processos em computadores diferentes. Normalmente, um processo de servidor de pipe nomeado cria um pipe nomeado com um nome conhecido ou um nome que deve ser comunicado a seus clientes. Um processo de cliente de pipe nomeado que conhece o nome do pipe pode abrir seu outro fim, sujeito às restrições de acesso especificadas pelo processo de servidor de pipe nomeado. Depois que o servidor e o cliente tiverem se conectado ao pipe, eles poderão trocar dados executando operações de leitura e gravação no pipe.

**Ponto-chave:** Pipes anônimos fornecem uma maneira eficiente de redirecionar a entrada ou saída padrão para processos filho no mesmo computador. Pipes nomeados fornecem uma interface de programação simples para transferir dados entre dois processos, independentemente de residirem no mesmo computador ou em uma rede. Para obter mais informações, consulte [pipes](pipes.md).

## <a name="using-rpc-for-ipc"></a>Usando RPC para IPC

O RPC permite que os aplicativos chamem funções remotamente. Portanto, o RPC torna o IPC tão fácil quanto chamar uma função. O RPC opera entre processos em um único computador ou em computadores diferentes em uma rede.

o RPC fornecido pelo Windows é compatível com o ambiente de computação distribuída (uso) do Open Software Foundation (DCE). Isso significa que os aplicativos que usam RPC são capazes de se comunicar com aplicativos em execução com outros sistemas operacionais que dão suporte à DCE. O RPC dá suporte automaticamente à conversão de dados para considerar diferentes arquiteturas de hardware e para ordenação de bytes entre ambientes não semelhantes.

Os clientes e servidores RPC estão firmemente acoplados, mas ainda mantêm alto desempenho. O sistema faz uso extensivo do RPC para facilitar uma relação de cliente/servidor entre diferentes partes do sistema operacional.

**Ponto-chave:** RPC é uma interface de nível de função, com suporte para conversão automática de dados e para comunicações com outros sistemas operacionais. Usando o RPC, você pode criar aplicativos distribuídos de alto desempenho e rigidamente acoplados. Para obter mais informações, consulte [Microsoft RPC Components](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>usando soquetes de Windows para IPC

Windows Sockets é uma interface independente de protocolo. Ele aproveita os recursos de comunicação dos protocolos subjacentes. no Windows sockets 2, um identificador de soquete pode, opcionalmente, ser usado como um identificador de arquivo com as funções de e/s de arquivo padrão.

Windows Os soquetes são baseados nos soquetes que primeiro foram populares pela Berkeley Software Distribution (BSD). um aplicativo que usa soquetes de Windows pode se comunicar com outras implementações de soquete em outros tipos de sistemas. No entanto, nem todos os provedores de serviço de transporte dão suporte a todas as opções disponíveis.

**ponto-chave:** o Windows sockets é uma interface independente de protocolo capaz de dar suporte aos recursos de rede atuais e emergentes. para obter mais informações, consulte [Windows sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
