---
title: Gerenciamento de transações (data Exchange)
description: Este tópico discute como um cliente pode enviar transações para obter dados e serviços do servidor.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Interface do Usuário,Dados Dinâmicos Exchange (DDE)
- Dados Dinâmicos Exchange (DDE), transações
- DDE (Dados Dinâmicos Exchange), transações
- troca de dados, Dados Dinâmicos Exchange (DDE)
- Windows Interface do Usuário,Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados Dinâmicos Exchange)
- DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange), transações
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados), transações
- troca de dados, Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados)
- Dados Dinâmicos Exchange (DDE), solicitação de transações
- DDE (Dados Dinâmicos Exchange), solicitação de transações
- DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange), transações de solicitação
- DDEML (biblioteca Dados Dinâmicos Exchange de gerenciamento), solicitação de transações
- Dados Dinâmicos Exchange (DDE), transações de transações de transações
- DDE (Dados Dinâmicos Exchange), transações de transações de transações
- DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange), transações de transações de
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados), transações de transações de
- Dados Dinâmicos Exchange (DDE), aconselhar transações
- DDE (Dados Dinâmicos Exchange), aconselhar transações
- DDEML (biblioteca de gerenciamento Dados Dinâmicos Exchange), aconselha transações
- DDEML (biblioteca Dados Dinâmicos Exchange de gerenciamento), aconselha transações
- Dados Dinâmicos Exchange (DDE), executar transações
- DDE (Dados Dinâmicos Exchange), executar transações
- DDEML (biblioteca de gerenciamento Dados Dinâmicos Exchange), executar transações
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados), executar transações
- Dados Dinâmicos Exchange (DDE), transações síncronas
- DDE (Dados Dinâmicos Exchange), transações síncronas
- DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange), transações síncronas
- DDEML (biblioteca Dados Dinâmicos Exchange de gerenciamento), transações síncronas
- Dados Dinâmicos Exchange (DDE), transações assíncronas
- DDE (Dados Dinâmicos Exchange), transações assíncronas
- DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange), transações assíncronas
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados), transações assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5065c9e909a4589cd7d2d157fc1151c2efd42a4ddfc3c29d84fd26f0ea184dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128568"
---
# <a name="transaction-management-data-exchange"></a>Gerenciamento de transações (data Exchange)

Depois de estabelecer uma conversa com um servidor, um cliente pode enviar transações para obter dados e serviços do servidor.

Os tópicos a seguir descrevem os tipos de transações que os clientes podem usar para interagir com um servidor.

-   [Solicitação de transação](#request-transaction)
-   [Transação transações de transações de transa](#poke-transaction)
-   [Aconselhar transação](#advise-transaction)
-   [Executar Transação](#execute-transaction)
-   [Transações síncronas e assíncronas](#synchronous-and-asynchronous-transactions)
-   [Controle de transação](#transaction-control)
-   [Classes de transação](#transaction-classes)
-   [Tipos de transação](#transaction-types)

## <a name="request-transaction"></a>Solicitação de transação

Um aplicativo cliente pode usar a transação [**XTYP \_ REQUEST**](xtyp-request.md) para solicitar um item de dados de um aplicativo de servidor. O cliente chama a [**função DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) especificando **SOLICITAÇÃO XTYP \_** como o tipo de transação e especificando o item de dados de que o aplicativo precisa.

A DDEML (biblioteca de gerenciamento de Dados Dinâmicos Exchange) passa a transação [**XTYP \_ REQUEST**](xtyp-request.md) para o servidor, especificando o nome do tópico, o nome do item e o formato de dados solicitados pelo cliente. Se o servidor for compatível com o tópico, o item e o formato solicitados, o servidor deverá retornar um identificador de dados que identifique o valor atual do item. O DDEML passa esse handle para o cliente como o valor de retorno de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). O servidor deverá retornar **NULL** se não tiver suporte para o tópico, item ou formato solicitado.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) usa o *parâmetro lpdwResult* para retornar um sinalizador de status de transação para o cliente. Se o servidor não processar a transação DE SOLICITAÇÃO [**XTYP, \_**](xtyp-request.md) **DdeClientTransaction** retornará **NULL** e *lpdwResult* aponta para o sinalizador \_ FNOTPROCESSED ou DDE \_ FBUSY DDE. Se o sinalizador FNOTPROCESSED de DDE for retornado, o cliente não poderá determinar por que o \_ servidor não processou a transação.

Se um servidor não dá suporte à transação [**de \_ SOLICITAÇÃO XTYP,**](xtyp-request.md) ele deve especificar o sinalizador de filtro SOLICITAÇÕES DE FALHA CBF na \_ função \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Esse sinalizador impede que o DDEML envie a transação para o servidor.

## <a name="poke-transaction"></a>Transação transações de transações de transa

Um cliente pode enviar dados não solicitados para um servidor usando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) para enviar uma transação [**XTYP? \_**](xtyp-poke.md)

O aplicativo cliente primeiro cria um buffer que contém os dados a enviar para o servidor e, em seguida, passa um ponteiro para o buffer como um parâmetro [**para DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Como alternativa, o cliente pode usar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para obter um identificador de dados que identifica os dados e, em seguida, passar o identificador para **DdeClientTransaction**. Em ambos os casos, o cliente também especifica o nome do tópico, o nome do item e o formato de dados quando chama **DdeClientTransaction**.

O DDEML passa a transação [**XTYP \_ CUT PARA**](xtyp-poke.md) O servidor, especificando o nome do tópico, o nome do item e o formato de dados solicitados pelo cliente. Para aceitar o item de dados e o formato, o servidor deve retornar O \_ FACK de DDE. Para rejeitar os dados, o servidor deve retornar DDE \_ FNOTPROCESSED. Se o servidor estiver muito ocupado para aceitar os dados, o servidor deverá retornar O DDE \_ FBUSY.

Quando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) retorna, o cliente pode usar o *parâmetro lpdwResult* para acessar o sinalizador transaction-status. Se o sinalizador for DDE \_ FBUSY, o cliente deverá enviar a transação novamente mais tarde.

Se um servidor não dá suporte à transação [**XTYP \_ IRON,**](xtyp-poke.md) ele deve especificar o sinalizador de filtro CBF \_ FAIL \_ WIDGETS [**em DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Esse sinalizador impede que o DDEML envie essa transação para o servidor.

## <a name="advise-transaction"></a>Aconselhar transação

Um aplicativo cliente pode usar o DDEML para estabelecer um ou mais links para itens em um aplicativo de servidor. Quando esse link é estabelecido, o servidor envia atualizações periódicas sobre o item vinculado para o cliente (normalmente, sempre que o valor do item associado ao aplicativo do servidor muda). A vinculação estabelece um loop de consultoria entre os dois aplicativos que permanecem em local até que o cliente o termine.

Há dois tipos de loops de consultoria: "quente" e "quente". Em um loop de consultoria a quente, o servidor envia imediatamente um identificador de dados que identifica o valor alterado. Em um loop de consultoria warm, o servidor notifica o cliente de que o valor do item foi alterado, mas não envia o alça de dados até que o cliente o solicita.

Um cliente pode solicitar um loop de consultoria a quente com um servidor especificando o tipo de transação [**\_ ADVSTART XTYP**](xtyp-advstart.md) em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Para solicitar um loop de consultoria warm, o cliente deve combinar o sinalizador NODATA XTYPF com o tipo de transação \_ **\_ ADVSTART XTYP.** Em ambos os eventos, o DDEML passa a transação **\_ ADVSTART XTYP** para a função de retorno de chamada Dados Dinâmicos Exchange (DDE) do servidor. A função de retorno de chamada DDE do servidor deve examinar os parâmetros que acompanham a transação **DO XTYP \_ ADVSTART** (incluindo o formato solicitado, o nome do tópico e o nome do item) e retornar **TRUE** para permitir que o loop de consultoria ou **FALSE** o negue.

Depois que um loop de consultoria tiver sido estabelecido, o aplicativo de servidor deverá chamar a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) sempre que o valor do item associado ao nome do item solicitado mudar. Essa chamada faz com que uma [**transação XTYP \_ ADVREQ**](xtyp-advreq.md) seja enviada para a própria função de retorno de chamada DDE do servidor. A função de retorno de chamada DDE do servidor deve retornar um identificador de dados que identifica o novo valor do item de dados. Em seguida, o DDEML notifica o cliente de que o item especificado foi alterado enviando a transação [**\_ ADVDATA XTYP**](xtyp-advdata.md) para a função de retorno de chamada DDE do cliente.

Se o cliente solicitou um loop de consultoria a quente, o DDEML passa o controle de dados para o item alterado para o cliente durante a transação [**XTYP \_ ADVDATA.**](xtyp-advdata.md) Caso contrário, o cliente pode enviar uma transação [**\_ DE SOLICITAÇÃO XTYP**](xtyp-request.md) para obter o handle de dados.

É possível que um servidor envie atualizações mais rapidamente do que um cliente possa processar os novos dados. A velocidade das atualizações pode ser um problema para um cliente que deve executar operações de processamento demoradas nos dados. Nesse caso, o cliente deve especificar o sinalizador ACKREQ do XTYPF \_ ao solicitar um loop de consultoria. Esse sinalizador faz com que o servidor aguarde até que o cliente confirme que recebeu e processou um item de dados antes que o servidor envie o próximo item de dados. Loops de consultoria estabelecidos com o sinalizador ACKREQ do XTYPF são mais robustos com servidores rápidos, mas ocasionalmente podem perder \_ atualizações. Loops de aviso estabelecidos sem o sinalizador ACKREQ do XTYPF têm a garantia de não perder atualizações, desde que o cliente continue \_ acompanhando o servidor.

Um cliente pode encerrar um loop de consultoria especificando o tipo de transação [**\_ ADVSTOP XTYP**](xtyp-advstop.md) em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Se um servidor não dá suporte a loops de consultoria, ele deve especificar o sinalizador de filtro CBF FAIL ADVISES na \_ \_ função [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Esse sinalizador impede que o DDEML envie as transações [**\_ ADVSTART**](xtyp-advstart.md) E [**XTYP \_ ADVSTOP**](xtyp-advstop.md) para o servidor.

## <a name="execute-transaction"></a>Executar Transação

Um cliente pode usar a [**transação EXECUTE \_ XTYP**](xtyp-execute.md) para fazer com que um servidor execute um comando ou uma série de comandos.

Para executar um comando de servidor, o cliente primeiro cria um buffer que contém uma cadeia de caracteres de comando para o servidor executar e, em seguida, passa um ponteiro para o buffer ou um identificador de dados que identifica o buffer quando ele chama [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Outros parâmetros necessários incluem o identificador de conversa, o identificador de cadeia de caracteres do nome do item, a especificação de formato e o tipo de [**transação EXECUTE \_ XTYP.**](xtyp-execute.md) Um aplicativo que cria um identificador de dados para transmitir dados de execução deve especificar **NULL** para o parâmetro *HszItem* da função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) e zero para o parâmetro *uFmt* .

O DDEML passa a transação [**XTYP \_ Execute**](xtyp-execute.md) para a função de retorno de chamada DDE do servidor e especifica o nome do formato, o identificador de conversa, o nome do tópico e o identificador de dados que identificam a cadeia de caracteres do comando. Se o servidor oferecer suporte ao comando, ele deverá usar a função [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obter um ponteiro para a cadeia de caracteres de comando, executar o comando e retornar \_ FACK DDE. Se o servidor não oferecer suporte ao comando ou não puder concluir a transação, ele deverá retornar \_ FNOTPROCESSED DDE. O servidor deve retornar \_ FBUSY DDE se estiver muito ocupado para concluir a transação.

Em geral, a função de retorno de chamada de um servidor deve processar a transação [**XTYP \_ Execute**](xtyp-execute.md) antes de retornar com as seguintes exceções:

1.  Quando o comando passado com a transação [**XTYP \_ Execute**](xtyp-execute.md) solicita que o servidor seja encerrado, o servidor não deve terminar até que sua função de retorno de chamada seja retornada do processamento **XTYP \_ Execute**.
2.  Se o servidor precisar executar uma operação, como processar uma caixa de diálogo ou uma transação DDE que possa causar problemas de recursão de DDEML, o servidor deverá retornar o \_ código de retorno de bloco CBR para bloquear a transação de execução, executar a operação e, em seguida, retomar o processamento da transação de execução.

Quando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) retorna, o cliente pode usar o parâmetro *lpdwResult* para acessar o sinalizador de status da transação. Se o sinalizador for DDE \_ FBUSY, o cliente deverá enviar a transação novamente mais tarde.

Se um servidor não oferecer suporte à transação de [**\_ execução de XTYP**](xtyp-execute.md) , ele deverá especificar o \_ sinalizador de filtro CBF falha de \_ execução na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Isso impede que o DDEML envie a transação para o servidor.

## <a name="synchronous-and-asynchronous-transactions"></a>Transações síncronas e assíncronas

Um cliente pode enviar transações síncronas ou assíncronas. Em uma transação síncrona, o cliente especifica um valor de tempo limite que indica a quantidade máxima de tempo que aguardará até que o servidor processe a transação. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) não retorna até que o servidor processe a transação, a transação falha ou o valor de tempo limite expire. O cliente especifica o valor de tempo limite quando chama **DdeClientTransaction**.

Durante uma transação síncrona, o cliente entra em um loop modal enquanto aguarda a transação ser processada. O cliente ainda pode processar a entrada do usuário, mas não pode enviar outra transação síncrona até que [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) retorne.

Um cliente envia uma transação assíncrona especificando o sinalizador assíncrono de tempo limite \_ em [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). A função retorna após o início da transação, passando um identificador de transação para o cliente. Quando o servidor conclui o processamento da transação assíncrona, o DDEML envia uma transação [**XTYP Transaction \_ \_ completa**](xtyp-xact-complete.md) para o cliente. Um dos parâmetros que o DDEML passa para o cliente durante a transação **de \_ \_ conclusão** de transações de XTYP é o identificador de transação. Ao comparar esse identificador de transação com o identificador retornado por **DdeClientTransaction**, o cliente identifica qual transação assíncrona o servidor concluiu o processamento.

Um cliente pode usar a função [**DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) como um auxílio no processamento de uma transação assíncrona. Essa função possibilita que um cliente associe um valor definido pelo aplicativo a um identificador de conversa e a uma transação. O cliente pode usar a função [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante a transação do [**XTYP \_ transação \_ completa**](xtyp-xact-complete.md) para obter o valor definido pelo aplicativo. Devido a essa função, um aplicativo não precisa manter uma lista de identificadores de transação ativa.

Quando um cliente conclui com êxito uma solicitação de dados usando uma transação síncrona, o DDEML não tem como saber quando o cliente terminou de usar os dados recebidos. O aplicativo cliente deve passar o identificador de dados recebido para a função [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , notificando o ddeml que o identificador não será mais usado. Os identificadores de dados retornados por transações síncronas são efetivamente pertencentes ao cliente.

Se um servidor não processar uma transação assíncrona em tempo hábil, o cliente poderá abandonar a transação chamando a função [**DdeAbandonTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) . O DDEML libera todos os recursos associados à transação e descarta os resultados da transação quando o servidor termina de processá-lo. Um tempo limite durante uma transação síncrona cancela efetivamente a transação.

O método de transação assíncrona é fornecido para aplicativos que devem enviar um alto volume de transações DDE enquanto executam simultaneamente uma quantidade significativa de processamento, como a realização de cálculos. O método assíncrono também é útil em aplicativos que devem parar de processar transações DDE temporariamente para que possam concluir outras tarefas sem interrupção. Na maioria das outras situações, um aplicativo deve usar o método síncrono.

As transações síncronas são mais simples de manter e são mais rápidas do que as transações assíncronas. No entanto, apenas uma transação síncrona pode ser executada de cada vez, enquanto muitas transações assíncronas podem ser executadas simultaneamente. Com transações síncronas, um servidor lento pode fazer com que um cliente permaneça ocioso enquanto está aguardando uma resposta. Além disso, transações síncronas fazem com que o cliente Insira um loop modal que poderia ignorar a filtragem de mensagens no próprio loop de mensagem do aplicativo.

Se o cliente tiver instalado um procedimento de gancho para filtrar mensagens (ou seja, especificado o \_ tipo de gancho MSGFILTER em uma chamada para a função [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) ), uma transação síncrona não fará com que o sistema ignore o procedimento de gancho. Quando um evento de entrada ocorre enquanto o cliente está aguardando a conclusão de uma transação síncrona, o procedimento de gancho recebe um \_ código de gancho MSGF DDEMGR. O principal perigo de usar um loop modal de transação síncrona é que um loop modal criado por uma caixa de diálogo pode interferir na operação. As transações assíncronas sempre devem ser usadas quando o DDEML estiver sendo usado por uma DLL.

## <a name="transaction-control"></a>Controle de transação

Um aplicativo pode suspender transações para sua função de retorno de chamada DDE dessas transações associadas a um identificador de conversa específico ou a todas as transações, independentemente do identificador de conversa. Esse recurso é útil quando um aplicativo recebe uma transação que requer processamento longo. Nesse caso, o aplicativo pode retornar o código de retorno de bloco de CBR \_ para suspender transações futuras associadas ao identificador de conversa da transação, para que o aplicativo fique livre para processar outras conversas.

Quando o processamento tiver sido concluído, o aplicativo chamará a função [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) para retomar as transações associadas à conversa suspensa. Chamar **DdeEnableCallback** faz com que o ddeml reenvie a transação que resultou no aplicativo suspendendo a conversa. Portanto, o aplicativo deve armazenar o resultado da transação de forma que possa obter e retornar o resultado sem reprocessar a transação.

Um aplicativo pode suspender todas as transações associadas a um identificador de conversa específico especificando o identificador e o \_ sinalizador de desabilitação do EC em uma chamada para [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Ao especificar um identificador **nulo** , um aplicativo pode suspender todas as transações de todas as conversas.

Quando uma conversa é suspensa, o DDEML salva transações para a conversa em uma fila de transações. Quando o aplicativo reabilita a conversa, o DDEML remove as transações salvas da fila e passa cada transação para a função de retorno de chamada apropriada. A capacidade da fila de transações é grande, mas um aplicativo deve reabilitar uma conversa suspensa assim que possível para evitar a perda de transações.

Um aplicativo pode retomar o processamento de transação usual especificando o \_ sinalizador ENABLEALL do EC em [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Para uma continuação mais controlada do processamento de transações, o aplicativo pode especificar o \_ sinalizador ENABLEONE do EC. Esse sinalizador remove uma transação da fila de transações e a passa para a função de retorno de chamada apropriada; Depois que essa transação tiver sido processada, todas as conversas serão desabilitadas novamente.

Se o \_ sinalizador ENABLEONE do EC e um identificador de conversa forem especificados na chamada para [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback), somente essa conversa será bloqueada depois que a transação for processada. Se um identificador de conversa **nulo** for especificado, todas as conversas serão bloqueadas depois que uma transação for processada em qualquer conversa.

## <a name="transaction-classes"></a>Classes de transação

O DDEML tem quatro classes de transações. Cada classe é identificada por uma constante que começa com o \_ prefixo XCLASS. As classes são definidas no arquivo de cabeçalho DDEML. O valor da classe é combinado com o valor do tipo de transação e é passado para a função de retorno de chamada DDE do aplicativo de recebimento.

A classe de uma transação determina o valor de retorno que uma função de retorno de chamada deve retornar se processar a transação. Os valores de retorno e os tipos de transação a seguir são associados a cada uma das quatro classes de transação.



| Classe                | Valor retornado                                                     | Transação                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_bool XCLASS         | **Verdadeiro** ou **falso**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ conectar**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| dados do XCLASS \_         | Um identificador de dados, o \_ código de retorno do bloco CBR ou **nulo**           | [**XTYP \_ ADVREQ**](xtyp-advreq.md)<br/> [**solicitação de XTYP \_**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| sinalizadores de XCLASS \_        | Um sinalizador de transação: DDE \_ FACK, DDE \_ FBUSY ou DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ executar**](xtyp-execute.md)<br/> [**XTYP \_**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| notificação de XCLASS \_ | Nenhum                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**confirmação do XTYP \_ Connect \_**](xtyp-connect-confirm.md)<br/> [**desconectar XTYP \_**](xtyp-disconnect.md)<br/> [**erro de XTYP \_**](xtyp-error.md)<br/> [**registro de XTYP \_**](xtyp-register.md)<br/> [**\_Cancelar registro do XTYP**](xtyp-unregister.md)<br/> [**\_transação XTYP \_ concluída**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Tipos de transação

Cada tipo de transação DDE tem um receptor e uma atividade associada que faz com que o DDEML gere cada tipo.



| Tipo de transação                                       | Receptor                   | Causa                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Cliente                     | Um servidor respondeu a uma transação [**XTYP \_ ADVREQ**](xtyp-advreq.md) retornando um identificador de dados.                                                                          |
| [**XTYP \_ ADVREQ**](xtyp-advreq.md)                    | Servidor                     | Um servidor chamado a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) , indicando que o valor de um item de dados em um loop de aviso foi alterado.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Servidor                     | Um cliente especificou o tipo de transação [**XTYP \_ ADVSTART**](xtyp-advstart.md) em uma chamada para a função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Servidor                     | Um cliente especificou o tipo de transação [**XTYP \_ ADVSTOP**](xtyp-advstop.md) em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**XTYP \_ conectar**](xtyp-connect.md)                  | Servidor                     | Um cliente chamou a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) e especificou um nome de serviço e um nome de tópico com suporte no servidor.                                            |
| [**confirmação do XTYP \_ Connect \_**](xtyp-connect-confirm.md) | Servidor                     | O servidor retornou **true** em resposta a uma transação [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .                            |
| [**desconectar XTYP \_**](xtyp-disconnect.md)            | Cliente/Servidor              | Um parceiro em uma conversa chamada função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) , fazendo com que os dois parceiros recebam essa transação.                                    |
| [**erro de XTYP \_**](xtyp-error.md)                      | Cliente/Servidor              | Ocorreu um erro crítico. O DDEML pode não ter recursos suficientes para continuar.                                                                                       |
| [**XTYP \_ executar**](xtyp-execute.md)                  | Servidor                     | Um cliente especificou o tipo de transação [**XTYP \_ Execute**](xtyp-execute.md) em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**MONITOR de XTYP \_**](xtyp-monitor.md)                  | Aplicativo de monitoramento de DDE | Ocorreu um evento DDE no sistema. Para obter mais informações sobre aplicativos de monitoramento de DDE, consulte [monitorando aplicativos](monitoring-applications.md).                       |
| [**XTYP \_**](xtyp-poke.md)                        | Servidor                     | Um cliente especificou o tipo de transação [**XTYP \_**](xtyp-poke.md) "em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                                    |
| [**registro de XTYP \_**](xtyp-register.md)                | Cliente/Servidor              | Um aplicativo de servidor usou a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar um nome de serviço.                                                                   |
| [**solicitação de XTYP \_**](xtyp-request.md)                  | Servidor                     | Um cliente especificou o tipo de transação de [**\_ solicitação XTYP**](xtyp-request.md) em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**\_Cancelar registro do XTYP**](xtyp-unregister.md)            | Cliente/Servidor              | Um aplicativo de servidor usou [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para cancelar o registro de um nome de serviço.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Servidor                     | Um cliente chamou a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , especificando **NULL** para o nome do serviço, o nome do tópico ou ambos. |
| [**\_transação XTYP \_ concluída**](xtyp-xact-complete.md)     | Cliente                     | Uma transação assíncrona, enviada quando o cliente especificou o sinalizador Async de tempo limite \_ em uma chamada para [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction), concluiu.         |



 

 

