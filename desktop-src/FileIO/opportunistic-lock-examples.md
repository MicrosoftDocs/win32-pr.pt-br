---
description: Diagramas de exibições de tráfego de rede para um bloqueio oportunista de nível 1, um bloqueio oportunista em lote e um bloqueio oportunista de filtro.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Exemplos de bloqueio oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505931"
---
# <a name="opportunistic-lock-examples"></a>Exemplos de bloqueio oportunista

Os exemplos a seguir mostram dados e movimentações de mensagem SMB conforme os bloqueios oportunistas são feitos e desfeitos. Observe que os clientes podem armazenar em cache dados de atributo de arquivo, bem como dados de arquivo.

Observe também que esses exemplos se baseiam em situações em que os aplicativos cliente estão solicitando bloqueios oportunistas de servidores remotos. Esses processos são iniciados automaticamente pelo redirecionador de rede e pelo servidor remoto — não há envolvimento direto pelo aplicativo cliente ou pelos aplicativos. Os processos descritos por esses exemplos podem ser generalizados em situações em que os aplicativos cliente locais estão solicitando diretamente os bloqueios oportunistas do sistema de arquivos local, com exceção de que nenhuma troca de dados pela rede está envolvida.

## <a name="level-1-opportunistic-lock"></a>Bloqueio oportunista de nível 1

O diagrama a seguir mostra uma exibição de tráfego de rede de um bloqueio oportunista de nível 1 em um arquivo. As setas indicam a direção da movimentação de dados, se houver.



| Evento | Cliente X                                          | Servidor                                   | Cliente Y                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Abre o arquivo, solicita o nível 1 Lock = =>          |                                          |                                                   |
| 2     |                                                   | <= = concede bloqueio oportunista de nível 1 |                                                   |
| 3     | Executa leitura, gravação e outras operações = => |                                          |                                                   |
| 4     |                                                   |                                          | <= = solicitações para abrir o arquivo                      |
| 5     |                                                   | <= = interrompe o bloqueio oportunista         |                                                   |
| 6     | Descarta dados de leitura antecipada                          |                                          |                                                   |
| 7     | Grava dados = =>                                |                                          |                                                   |
| 8     | Envia mensagem de "fechamento" ou "concluída" = =>            |                                          |                                                   |
| 9     |                                                   | Ok operação de abertura = =>              |                                                   |
| 10    | Executa leitura, gravação e outras operações = => |                                          | <= = executa operações de leitura, gravação e outras |



 

No evento 1, Client X abre um arquivo e, como parte da operação aberta, solicita um bloqueio oportunista de nível 1 no arquivo. No evento 2, o servidor concede o bloqueio de nível 1 porque nenhum outro cliente tem o arquivo aberto. O cliente continua acessando o arquivo da maneira usual no evento 3.

No evento 4, o cliente Y tenta abrir o arquivo e solicita um bloqueio oportunista. O servidor vê que o cliente X tem o arquivo aberto. O servidor ignora a solicitação de Y enquanto o cliente X libera os dados de gravação e abandona seu cache de leitura para o arquivo.

O servidor força o X a limpar enviando para X uma mensagem SMB rompendo o bloqueio oportunista, evento 5. O cliente X "silenciosamente" descarta todos os dados de leitura antecipada; em outras palavras, esse processo não gera tráfego de rede. No evento 7, o cliente X grava os dados de gravação em cache no servidor. Quando o cliente X é concluído gravando dados em cache no servidor, o cliente X envia uma mensagem de "fechamento" ou "concluída" para o servidor, evento 8.

Depois que o servidor tiver sido notificado de que o cliente X foi concluído, liberando seu cache de gravação para o servidor ou fechou o arquivo, o servidor poderá abrir o arquivo para o cliente Y, no evento 9. Como o servidor agora tem dois clientes com o mesmo arquivo aberto, ele concede um bloqueio oportunista a nenhum. Ambos os clientes passam a ler o arquivo e uma ou nenhuma gravação no arquivo.

## <a name="batch-opportunistic-lock"></a>Bloqueio oportunista em lote

O diagrama a seguir mostra uma exibição de tráfego de rede de um bloqueio oportunista em lote. As setas indicam a direção da movimentação de dados, se houver.



| Evento | Cliente X                               | Servidor                                 | Cliente Y                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Abre o arquivo, solicita bloqueio do lote = => |                                        |                                                   |
| 2     |                                        | <= = concede bloqueio oportunista em lote |                                                   |
| 3     | Arquivo de leituras = =>                      |                                        |                                                   |
| 4     |                                        | <= = envia dados                      |                                                   |
| 5     | Fecha o arquivo                            |                                        |                                                   |
| 6     | Abre o arquivo                             |                                        |                                                   |
| 7     | Pesquisa dados                      |                                        |                                                   |
| 8     | Leituras de dados = =>                      |                                        |                                                   |
| 9     |                                        | <= = envia dados                      |                                                   |
| 10    | Fecha o arquivo                            |                                        |                                                   |
| 11    |                                        |                                        | <= = abre o arquivo                                 |
| 12    |                                        | <= = interrompe o bloqueio oportunista       |                                                   |
| 13    | Fecha o arquivo = =>                     |                                        |                                                   |
| 14    |                                        | Ok operação de abertura = =>            |                                                   |
| 15    |                                        |                                        | <= = executa operações de leitura, gravação e outras |



 

No bloqueio oportunista em lote, o cliente X abre um arquivo, evento 1, e o servidor concede ao cliente X um bloqueio de lote no evento 2. O cliente X tenta ler dados, evento 3, para o qual o servidor responde com os dados, evento 4.

O evento 5 mostra o bloqueio oportunista em lote no trabalho. O aplicativo no cliente X fecha o arquivo. No entanto, o redirecionador de rede filtra a operação de fechamento e não transmite uma mensagem de fechamento, realizando assim um fechamento "silencioso". O redirecionador de rede pode fazer isso porque o cliente X tem Propriedade exclusiva do arquivo. Posteriormente, no evento 6, o aplicativo reabrirá o arquivo. Novamente, não há fluxos de dados na rede. No que diz respeito ao servidor, esse cliente teve o arquivo aberto desde o evento 2.

Os eventos 7, 8 e 9 mostram o curso normal do tráfego de rede. No evento 10, ocorre outro fechamento silencioso.

No evento 11, o cliente Y tenta abrir o arquivo. A exibição do arquivo do servidor é que o cliente X o abriu, mesmo que o aplicativo no cliente X o tenha fechado. Portanto, o servidor envia uma mensagem que quebra o bloqueio oportunista para o cliente X. o cliente X envia agora a mensagem de fechamento pela rede, evento 13. O evento 14 é exibido conforme o servidor abre o arquivo para o cliente Y. O aplicativo no cliente X fechou o arquivo, portanto, ele não faz mais transferências para ou do servidor para esse arquivo. O cliente Y inicia as transferências de dados como de costume no evento 15.

Entre o tempo, o cliente X recebe o bloqueio no arquivo no evento 2 e o fechamento final no evento 13, todos os dados de arquivo que o cliente armazenou em cache são válidos, apesar das operações de abertura e fechamento do aplicativo intermediário. No entanto, depois que o bloqueio oportunista for interrompido, os dados armazenados em cache não poderão ser considerados válidos.

## <a name="filter-opportunistic-lock"></a>Filtrar bloqueio oportunista

O diagrama a seguir mostra uma exibição de tráfego de rede de um bloqueio oportunista de filtro. As setas indicam a direção da movimentação de dados, se houver.



| Evento | Cliente X                                | Servidor                   | Cliente Y                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Abre o arquivo sem direitos de acesso = => |                          |                             |
| 2     |                                         | <= = abre o arquivo    |                             |
| 3     | Solicita bloqueio de filtro = =>              |                          |                             |
| 4     |                                         | <= = concede bloqueio       |                             |
| 5     | Abre o arquivo para leitura = =>           |                          |                             |
| 6     |                                         | <= = reabre o arquivo  |                             |
| 7     | Lê dados usando o identificador de leitura = => |                          |                             |
| 8     |                                         | <= = envia dados        |                             |
| 9     |                                         | <= = envia dados        |                             |
| 10    |                                         | <= = envia dados        |                             |
| 11    |                                         |                          | <= = abre o arquivo       |
| 12    |                                         | Abre o arquivo = =>    |                             |
| 13    |                                         |                          | <= = solicitar bloqueio de filtro |
| 14    |                                         | Nega bloqueio de filtro = => |                             |
| 15    |                                         |                          | <= = lê dados           |
| 16    |                                         | Envia dados = =>        |                             |
| 17    | Leituras (em cache) de dados                     |                          |                             |
| 18    | Fecha o arquivo = =>                      |                          |                             |
| 19    |                                         |                          | <= = fecha o arquivo          |



 

No bloqueio oportunista do filtro, o cliente X abre um arquivo, evento 1, e o servidor responde no evento 2. Em seguida, o cliente solicita um bloqueio oportunista de filtro no evento 3, seguido pelo servidor que concede o bloqueio oportunista no evento 4. O cliente X abre o arquivo novamente para leitura no evento 5, ao qual o servidor responde no evento 6. Em seguida, o cliente tenta ler os dados, aos quais o servidor responde com os dados, evento 8.

O evento 9 mostra o bloqueio oportunista do filtro no trabalho. O servidor lê a frente do cliente e envia os dados pela rede, mesmo que o cliente não o tenha solicitado. O cliente armazena em cache os dados. No evento 10, o servidor também prevê uma solicitação futura de dados e envia outra parte do arquivo para o cliente armazenar em cache.

No evento 11 e 12, outro cliente, Y, abre o arquivo. O cliente Y também solicita um bloqueio oportunista de filtro. No evento 14, o servidor o nega. No evento 15, Client Y solicita dados, que o servidor envia no evento 16. Nenhum deles afeta o cliente X. A qualquer momento, outro cliente pode abrir esse arquivo para acesso de leitura. Nenhum outro cliente afeta o bloqueio de filtro do cliente X.

O evento 17 mostra dados de leitura do cliente X. No entanto, como o servidor já enviou os dados e o cliente o armazenou em cache, nenhum tráfego cruza a rede.

Neste exemplo, o cliente X nunca tenta ler todos os dados no arquivo, de modo que o Read-Ahead indicado pelos eventos 9 e 10 é "desperdiçado"; ou seja, os dados nunca são realmente usados. Essa é uma perda aceitável porque o Read-Ahead tem o SPED up do aplicativo.

No evento 18, o cliente X fecha o arquivo. O redirecionador de rede do cliente abandona os dados armazenados em cache. O servidor fecha o arquivo.

 

 



