---
title: Conceitos básicos
description: Este tópico discute os principais conceitos relacionados à troca de dados dinâmicas.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Windows Interface do usuário, troca dinâmica de dados (DDE)
- Windows Interface do usuário, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- troca dinâmica de dados (DDE), interação do servidor cliente
- DDE (troca dinâmica de dados), interação do servidor cliente
- troca de dados, troca dinâmica de dados (DDE)
- data exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- troca dinâmica de dados (DDE), aplicativos cliente
- DDE (troca dinâmica de dados), aplicativos cliente
- troca dinâmica de dados (DDE), aplicativos de servidor
- DDE (troca dinâmica de dados), aplicativos de servidor
- troca dinâmica de dados (DDE), funções de retorno de chamada
- DDE (troca dinâmica de dados), funções de retorno de chamada
- troca dinâmica de dados (DDE), transações
- DDE (troca dinâmica de dados), transações
- troca dinâmica de dados (DDE), nomes de serviço
- DDE (troca dinâmica de dados), nomes de serviço
- troca dinâmica de dados (DDE), nomes de item
- DDE (troca dinâmica de dados), nomes de item
- troca dinâmica de dados (DDE), nomes de tópico
- DDE (troca dinâmica de dados), nomes de tópico
- troca dinâmica de dados (DDE), tópico do sistema
- DDE (troca dinâmica de dados), tópico do sistema
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), inicialização
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), inicialização
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), funções de retorno de chamada
- DDEML (troca dinâmica de dados biblioteca de gerenciamento), funções de retorno de chamada
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de cadeia de caracteres
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), gerenciamento de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae271c359afd571cf6c51fb3387a15f1496416e5eb54b055ef518fd213f30fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128618"
---
# <a name="basic-concepts-dde"></a>Conceitos básicos (DDE)

esses conceitos são fundamentais para entender troca dinâmica de dados (DDE) e a biblioteca de gerenciamento de troca dinâmica de dados (DDEML).

-   [Interação de cliente e servidor](#client-and-server-interaction)
-   [Transações e a função de retorno de chamada DDE](#transactions-and-the-dde-callback-function)
-   [Nomes de serviço, nomes de tópico e nomes de item](#service-names-topic-names-and-item-names)
-   [Tópico do sistema](#system-topic)
-   [Inicialização](#initialization)
-   [Função de retorno de chamada](#callback-function)
-   [Gerenciamento de cadeia de caracteres](#string-management)
-   [DDEML e threads](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interação de cliente e servidor

O DDE sempre ocorre entre um aplicativo cliente e um aplicativo de servidor. O *aplicativo cliente DDE* inicia o Exchange estabelecendo uma conversa com o servidor para enviar transações ao servidor. Uma transação é uma solicitação de dados ou serviços. O *aplicativo do servidor DDE* responde às transações fornecendo dados ou serviços ao cliente. Por exemplo, um aplicativo de gráficos pode conter um gráfico de barras que representa os lucros trimestrais de uma empresa, mas os dados do grafo de barras podem estar contidos em um aplicativo de planilha. Para obter os valores de lucro mais recentes, o aplicativo de gráficos (o cliente) pode estabelecer uma conversa com o aplicativo de planilha (o servidor). O aplicativo gráfico poderia então enviar uma transação para o aplicativo de planilha, solicitando os valores de lucro mais recentes.

Um servidor pode ter muitos clientes ao mesmo tempo e um cliente pode solicitar dados de vários servidores. Um aplicativo também pode ser um cliente e um servidor. O cliente ou o servidor pode encerrar a conversa a qualquer momento.

## <a name="transactions-and-the-dde-callback-function"></a>Transações e a função de retorno de chamada DDE

O DDEML notifica um aplicativo sobre a atividade DDE que afeta o aplicativo enviando transações para a função de retorno de chamada DDE do aplicativo. Uma *transação DDE* é semelhante a uma mensagem que é uma constante nomeada acompanhada por outros parâmetros que contêm informações adicionais sobre a transação.

O DDEML passa uma transação para uma função de retorno de chamada DDE definida pelo aplicativo que executa uma ação apropriada ao tipo de transação. Por exemplo, quando um aplicativo cliente tenta estabelecer uma conversa com um aplicativo de servidor, o cliente chama a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) . Essa função faz com que o DDEML envie uma transação [**XTYP \_ Connect**](xtyp-connect.md) para a função de retorno de chamada DDE do servidor. A função de retorno de chamada pode permitir a conversa retornando **true** para o ddeml, ou pode negar a conversa retornando **false**. Para obter uma discussão detalhada sobre as transações, consulte [Gerenciamento de transações](transaction-management.md).

## <a name="service-names-topic-names-and-item-names"></a>Nomes de serviço, nomes de tópico e nomes de item

Um servidor DDE usa um nome de serviço de hierarquia de três níveis (chamado de "nome do aplicativo" na documentação DDE anterior), nome do tópico e nome do item para identificar exclusivamente uma unidade de dados que o servidor pode trocar durante uma conversa.

Um *nome de serviço* é uma cadeia de caracteres que um aplicativo de servidor responde quando um cliente tenta estabelecer uma conversa com o servidor. Um cliente deve especificar esse nome de serviço para estabelecer uma conversa com o servidor. Embora um servidor possa responder a muitos nomes de serviço, a maioria dos servidores responde a apenas um nome.

Um *nome de tópico* é uma cadeia de caracteres que identifica um contexto de dados lógicos. Para servidores que operam em documentos baseados em arquivo, os nomes de tópico são normalmente nomes de arquivos; para outros servidores, eles são cadeias de caracteres específicas do aplicativo. Um cliente deve especificar um nome de tópico junto com o nome do serviço de um servidor ao tentar estabelecer uma conversa com um servidor.

Um *nome de item* é uma cadeia de caracteres que identifica uma unidade de dados que um servidor pode passar para um cliente durante uma transação. Por exemplo, um nome de item pode identificar um inteiro, uma cadeia de caracteres, vários parágrafos de texto ou um bitmap.

Os nomes de serviço, tópico e item permitem que o cliente estabeleça uma conversa com um servidor e receba dados do servidor.

## <a name="system-topic"></a>Tópico do sistema

O tópico System fornece um contexto para obter informações de interesse geral para qualquer cliente DDE. É recomendável que os aplicativos de servidor ofereçam suporte ao tópico do sistema em todos os momentos. O tópico System é definido em DDEML. Arquivo de cabeçalho H como \_ tópico SZDDESYS.

Para determinar quais servidores estão presentes e os tipos de informações que eles podem fornecer, um aplicativo cliente pode solicitar uma conversa no tópico do sistema ao iniciar, definindo o nome do dispositivo como **nulo**. Essas conversas de curinga são dispendiosas em termos de desempenho do sistema, portanto, devem ser mantidas em um mínimo. Para obter mais informações sobre como iniciar conversas DDE, consulte [Gerenciamento de conversa](conversation-management.md).

Um servidor deve dar suporte aos seguintes nomes de item no tópico do sistema e em qualquer outro nome de item que seja útil para um cliente.



| Item                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_lista de itens do SZDDE \_    | Uma lista de itens com suporte em um tópico que não é do sistema. (Essa lista pode variar de momentos para momento e de tópico para tópico.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_formatos de item SZDDESYS \_  | Uma lista delimitada por tabulação de cadeias de caracteres que representa todos os formatos de área de transferência possivelmente compatíveis com o aplicativo de serviço. Cadeias de caracteres que representam formatos de área de transferência predefinidos são equivalentes aos valores de CF \_ com o prefixo "CF \_ " removido. Por exemplo, o formato de texto do CF \_ é representado pela cadeia de caracteres "text". Essas cadeias de caracteres devem ser maiúsculas para identificá-las ainda mais como formatos predefinidos. A lista de formatos deve aparecer na ordem do conteúdo mais rico para o mais rico em conteúdo. Para obter mais informações sobre formatos de área de transferência e dados de renderização, consulte [área de transferência](clipboard.md).<br/> |
| \_ajuda do item SZDDESYS \_     | Informações legíveis ao usuário de interesse geral. Esse item deve conter, no mínimo, informações sobre como usar os recursos de DDE do aplicativo de servidor. Essas informações podem incluir, mas não se limitando a, como especificar itens dentro de tópicos, o que executa cadeias de caracteres que o servidor pode executar, o que as transações de busca são permitidas e como encontrar ajuda em outros itens de tópico do sistema.                                                                                                                                                                                                                           |
| SZDDESYS \_ item \_ RTNMSG   | Detalhes de suporte para a mensagem de [**\_ \_ confirmação de DDE do WM**](wm-dde-ack.md) usada mais recentemente. Esse item é útil quando são necessários mais de 8 bits de dados de retorno específicos do aplicativo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_status do item de SZDDESYS \_   | Uma indicação do status atual do servidor. Normalmente, esse item dá suporte apenas ao \_ formato de texto do CF e contém a cadeia de caracteres pronta ou ocupada.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SZDDESYS \_ item \_ SYSITEMS | Uma lista dos itens com suporte no tópico System por este servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_Tópicos do item SZDDESYS \_   | Uma lista dos tópicos com suporte no servidor na hora atual. (Essa lista pode variar de um momento até o momento.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Esses nomes de item são valores definidos no DDEML. Arquivo de cabeçalho H. Para obter identificadores de cadeias de caracteres para essas cadeias, um aplicativo deve usar as funções de gerenciamento de cadeia de caracteres de DDEML, assim como faria para qualquer outra cadeia de caracteres em um aplicativo DDEML. Para obter mais informações sobre o gerenciamento de cadeias de caracteres, consulte [Gerenciamento de cadeia](#string-management).

## <a name="initialization"></a>Inicialização

Antes de chamar qualquer outra função de DDEML, um aplicativo deve chamar a função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . O **DdeInitialize** Obtém um identificador de instância para o aplicativo, registra a função de retorno de chamada DDE do aplicativo com o DDE e especifica os sinalizadores de filtro de transação para a função de retorno de chamada.

Cada instância de um aplicativo ou uma DLL deve passar seu identificador de instância como o parâmetro *idInst* para qualquer outra função de ddeml que o exija. A finalidade de várias instâncias de DDEML é dar suporte a DLLs que devem usar o DDEML ao mesmo tempo em que um aplicativo o está usando. Um aplicativo não deve usar mais de uma instância do DDEML.

Os *filtros de transação* otimizam o desempenho do sistema impedindo que o ddeml transmita transações indesejadas para a função de retorno de chamada DDE do aplicativo. Um aplicativo define os filtros de transação no parâmetro [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* . Um aplicativo deve especificar um sinalizador de filtro de transação para cada tipo de transação que ele não processa em sua função de retorno de chamada. Um aplicativo pode alterar seus filtros de transação com uma chamada subsequente para **DdeInitialize**. Para obter mais informações sobre transações, consulte [Gerenciamento de transações](transaction-management.md).

O exemplo a seguir mostra como inicializar um aplicativo para usar o DDEML.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Um aplicativo deve chamar a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) quando ele não vai mais usar o ddeml. Essa função encerra todas as conversas abertas no momento para o aplicativo e libera os recursos de DDEML que o sistema alocou para o aplicativo.

## <a name="callback-function"></a>Função de retorno da chamada

Um aplicativo que usa o DDEML deve fornecer uma função de retorno de chamada que processa os eventos DDE que afetam o aplicativo. O DDEML notifica um aplicativo sobre tais eventos enviando transações para a função de retorno de chamada DDE do aplicativo. As transações que uma função de retorno de chamada recebe dependem de qual filtro de retorno de chamada sinaliza o aplicativo especificado em [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) e se o aplicativo é um cliente, um servidor ou ambos. Para obter mais informações, consulte [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

O exemplo a seguir mostra a estrutura geral de uma função de retorno de chamada para um aplicativo cliente típico.


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



O parâmetro *uType* especifica o tipo de transação enviado à função de retorno de chamada pelo ddeml. Os valores dos parâmetros restantes dependem do tipo de transação. Os tipos de transação e os eventos que os geram são descritos nos tópicos a seguir. Para obter informações detalhadas sobre cada tipo de transação, consulte [Gerenciamento de transações](transaction-management.md).

## <a name="string-management"></a>Gerenciamento de cadeia de caracteres

Para executar uma tarefa DDE, muitas funções de DDEML exigem acesso a cadeias de caracteres. Por exemplo, um cliente deve especificar um nome de serviço e um nome de tópico ao chamar a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) para solicitar uma conversa com um servidor. Um aplicativo especifica uma cadeia de caracteres passando um identificador de cadeia de caracteres (HSZ) em vez de um ponteiro em uma função DDEML. Um *identificador de cadeia de caracteres* é um valor **DWORD** , atribuído pelo sistema, que identifica uma cadeia de caracteres.

Um aplicativo pode obter um identificador de cadeia de caracteres para uma cadeia de caracteres específica chamando a função [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) . Essa função registra a cadeia de caracteres com o sistema e retorna um identificador de cadeia de caracteres para o aplicativo. O aplicativo pode passar o identificador para as funções DDEML que devem acessar a cadeia de caracteres. O exemplo a seguir obtém identificadores de cadeia de caracteres para a cadeia de caracteres do tópico do sistema e a cadeia de nome do serviço.


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



O parâmetro *idInst* no exemplo anterior especifica o identificador de instância obtido pela função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

A função de retorno de chamada DDE de um aplicativo recebe um ou mais identificadores de cadeia de caracteres durante a maioria das transações DDE. Por exemplo, um servidor recebe dois identificadores de cadeia de caracteres durante a transação de [**\_ solicitação XTYP**](xtyp-request.md) : um identifica uma cadeia de caracteres que especifica um nome de tópico e o outro identifica uma cadeia de caracteres que especifica um nome de item. Um aplicativo pode obter o comprimento da cadeia de caracteres que corresponde a um identificador de cadeia de caracteres e copiar a cadeia de caracteres para um buffer definido pelo aplicativo chamando a função [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , conforme mostrado no exemplo a seguir.


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



Um identificador de cadeia de caracteres específica de instância não pode ser mapeado do identificador de cadeia de caracteres para cadeia de caracteres e voltar para identificador de cadeia de caracteres Por exemplo, embora [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crie uma cadeia de caracteres de um identificador de cadeia de caracteres e, em seguida, [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) cria um identificador de cadeia de caracteres a partir dessa cadeia de caracteres, os dois identificadores não são os mesmos, conforme mostrado no exemplo a seguir.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Para comparar os valores de dois identificadores de cadeia de caracteres, use a função [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .

Um identificador de cadeia de caracteres passado para a função de retorno de chamada DDE de um aplicativo se torna inválido quando a função de retorno de chamada retorna. Um aplicativo pode salvar um identificador de cadeia de caracteres para uso após a função de retorno de chamada retornar usando a função [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .

Quando um aplicativo chama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), o sistema insere a cadeia de caracteres especificada em uma tabela de cadeia de caracteres e gera um identificador que ele usa para acessar a cadeia de caracteres. O sistema também mantém uma contagem de uso para cada cadeia de caracteres na tabela de cadeias de caracteres.

Quando um aplicativo chama [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) e especifica uma cadeia de caracteres que já existe na tabela, o sistema incrementa a contagem de uso em vez de adicionar outra ocorrência da cadeia de caracteres. (Um aplicativo também pode incrementar a contagem de uso usando [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) Quando um aplicativo chama a função [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , o sistema decrementa a contagem de uso.

Uma cadeia de caracteres é removida da tabela quando sua contagem de uso é igual a zero. Como mais de um aplicativo pode obter o identificador para uma cadeia de caracteres específica, um aplicativo não deve liberar um identificador de cadeia de caracteres mais vezes do que criou ou manteve o identificador. Caso contrário, o aplicativo pode fazer com que a cadeia de caracteres seja removida da tabela, negando a outros aplicativos acesso à cadeia de caracteres.

As funções de gerenciamento de cadeia de caracteres de DDEML são baseadas no Gerenciador de Atom e estão sujeitas às mesmas restrições de tamanho que são Atoms.

## <a name="ddeml-and-threads"></a>DDEML e threads

A função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra um aplicativo com o ddeml, criando uma instância de ddeml. Uma instância de DDEML é baseada em thread, associada ao thread que chamou **DdeInitialize**.

Todas as chamadas de função DDEML para objetos que pertencem a uma instância de DDEML devem ser feitas no mesmo thread que chamou [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) para criar a instância. Se você chamar uma função DDEML de um thread diferente, a função falhará. Você não pode acessar uma conversa de DDEML de um thread que não seja aquele que alocou a conversa.

 

