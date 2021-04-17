---
title: Ciclo de vida de um trabalho do BITS
description: O ciclo de vida de um trabalho BITS começa quando você cria um trabalho.
ms.assetid: b765a8ef-74bd-475e-9cd9-e9e2cf4f0305
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c6ac23c598d28681968e9c0cbed776ba24c57e98
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105756076"
---
# <a name="bits-job-states"></a>Estados de trabalho do BITS
Há quatro classes de [**Estados**](/windows/desktop/api/Bits/ne-bits-bg_job_state)do bits: Iniciando, ação, transferido e final. À medida que um trabalho é executado, ele faz a transição entre os Estados nas diferentes classes de estado. Quando um trabalho está em um estado final, ele não sai do estado final e não aparecerá em uma enumeração de [trabalho](/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-enumjobs).

## <a name="state-changing-methods"></a>Métodos de alteração de estado
Há quatro métodos de alteração de estado em um trabalho: [**Cancelar**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel), [**concluir**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete), [**retomar**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)e [**suspender**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend). Desde que um trabalho não esteja em um estado final, você pode chamar qualquer um dos métodos de alteração de estado. 

O método [**Suspend**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend) é usado para alternar um trabalho para o estado suspenso. Quando um trabalho for suspenso, todas as suas transferências serão interrompidas e não serão retomadas até que você chame resume.
Um trabalho que já está suspenso simplesmente permanecerá suspenso.

O método [**resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) é usado para iniciar um trabalho suspenso. Os trabalhos em um erro ou estado de erro transitório serão configurados para serem repetidos. Os trabalhos que estão em um estado de ação no momento permanecerão nesse estado.

O método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) é usado para cancelar um trabalho. O estado será alternado para cancelado. Todos os arquivos que estão sendo transferidos não serão concluídos. Todos os arquivos transferidos por completo e parcialmente transferidos serão excluídos.

O método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) concluirá uma transferência. Todos os arquivos totalmente baixados serão mantidos; os arquivos que não forem totalmente transferidos serão excluídos.

Você deve chamar Cancel ou Complete para mover seu trabalho para um estado final e ser limpo. Os trabalhos que não são transferidos para um estado final perderão os recursos do sistema. Eventualmente, o BITS cancelará automaticamente os trabalhos antigos. O [JobInactivityTimeout](/windows/desktop/Bits/group-policies) padrão é cancelar trabalhos após 90 dias.


## <a name="starting-state"></a>Estado inicial 
O estado inicial é **suspenso**. A partir daqui, você pode adicionar arquivos ao trabalho e definir as propriedades do trabalho e do arquivo. Para iniciar uma transferência de trabalho, chame resume no trabalho. Se você retomar um trabalho sem arquivos, ele retornará um BG_E_EMPTY código de erro e o trabalho permanecerá suspenso.

## <a name="action-states"></a>Estados de ação
Os Estados **enfileirados**, **conectando** e **transferindo** mostram a atividade interna atual do seu trabalho. Um trabalho que está na fila está pronto para ser agendado, possivelmente aguardando o Agendador de BITS ou aguardando que o usuário faça logon. Um trabalho que está se CONECTAndo está tentando se conectar ao servidor para iniciar a transferência de arquivos. Um trabalho que está sendo transferido está ativamente carregando ou baixando seus arquivos.

O estado de **erro transitório** significa que o trabalho tentou e não transferiu o arquivo. Isso pode ser por motivos de diretiva de rede; o trabalho pode estar bloqueado porque a rede atual é muito cara. Ele também pode ser bloqueado por motivos do sistema, como o sistema está em modo de economia de bateria ou de jogo, ou porque não há nenhuma conectividade com a Internet. 

Os trabalhos no estado de erro transitório serão repetidos automaticamente por BITS quando apropriado. O BITS inclui um valor de [MinimumRetryDelay](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar quando um trabalho é repetido e quando o bits, por fim, interromperá a repetição.


## <a name="transferred-states"></a>Estados transferidos
Os Estados transferidos ocorrem quando não há mais transferência a ser feita. Você deve cancelar ou concluir um trabalho nesse estado. Você também pode adicionar mais arquivos para transferir e chamar resume (), mas essa não é uma prática comum.

O estado de **erro** ocorre quando uma transferência é feita (ela não será repetida), mas não foi totalmente bem-sucedida. Todos os arquivos devem ser transferidos para serem bem-sucedidos; Se qualquer um tiver falhado permanentemente, o trabalho estará em erro. Normalmente, você chamará cancelar ou concluir para mover o trabalho para um estado final. A diferença prática é que quando você chama cancelar, qualquer arquivo transferido com êxito será excluído, mas se você chamar concluir, qualquer arquivo transferido com êxito não será excluído.

Os motivos para serem em um estado de erro incluem 
* Ficar muito longo em um estado de erro transitório (além da configuração de [NoProgressTimeout](/windows/desktop/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) ).
* Obter um erro de BG_E_TOKEN_REQUIRED e precisar de assistência com [tokens auxiliares](/windows/desktop/Bits/helper-tokens-for-bits-transfer-jobs)

É uma prática comum reconfigurar um trabalho de erro e, em seguida, chamar resume para repetir o trabalho. Por exemplo, seu aplicativo pode precisar atualizar o nome remoto de um arquivo por meio de [Setremotename](/windows/desktop/api/bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename).

O estado **transferido** ocorre quando uma transferência é feita e ela foi bem-sucedida. Você deve chamar Complete para finalizar o trabalho; para baixar trabalhos, os arquivos baixados não estarão disponíveis até que você chame concluir. A exceção a essa regra são os trabalhos que são trabalhos de alto desempenho (e você ainda deve chamar concluído).

## <a name="final-states"></a>Estados finais
Quando um trabalho está em um estado final, você não pode chamar nenhum dos métodos de alteração de estado. O trabalho será **confirmado** depois que você chamar Complete () e todos os arquivos baixados concluídos estarão disponíveis. O trabalho será **cancelado** depois que você chamar Cancel () e todos os arquivos baixados serão excluídos. 


## <a name="life-cycle-of-a-bits-job"></a>Ciclo de vida de um trabalho do BITS

O ciclo de vida de um trabalho BITS começa quando você cria um trabalho. Um trabalho é um contêiner que contém um ou mais arquivos a serem transferidos. Um trabalho também tem propriedades que especificam como o BITS transfere os arquivos e interage com seu aplicativo. Por exemplo, você pode especificar a prioridade do trabalho, se o trabalho é um trabalho de upload ou de download e para quais eventos você deseja receber a notificação.

Depois de criar o trabalho, adicione um ou mais arquivos (os trabalhos de carregamento podem conter apenas um arquivo) para o trabalho e altere qualquer um dos valores de propriedade conforme apropriado para seu aplicativo. Ao adicionar um arquivo ao trabalho, especifique o nome local (cliente) e remoto (servidor) do arquivo. O nome do arquivo remoto deve usar o protocolo HTTP, HTTPS ou SMB. Os arquivos em um trabalho são processados sequencialmente (primeiro a entrar, primeiro a sair).

O BITS suspende automaticamente os trabalhos quando eles são criados. Você deve retomar o trabalho para ativá-lo na fila de transferência. Você pode suspender ou retomar um trabalho a qualquer momento. Retomar o trabalho move o trabalho do estado suspenso para o estado enfileirado. O trabalho permanece no estado Enfileirado até que o Agendador determine que é a vez de transferir os arquivos do trabalho. Todos os trabalhos de primeiro plano são executados simultaneamente com um trabalho em segundo plano. O BITS processa em série os arquivos em trabalhos em primeiro plano.

Quando é uma vez que um trabalho é transferido para transferir arquivos, o trabalho é movido para o estado de conexão enquanto o BITS se conecta ao servidor remoto (especificado no nome do arquivo remoto). Se o BITS for capaz de se conectar ao servidor remoto, o trabalho passará para o estado de transferência, onde permanecerá até que sua fatia de tempo termine, a transferência seja concluída, um erro ocorra ou o aplicativo suspende o trabalho.

O trabalho é movido entre os Estados na fila, na conexão e na transferência até que o BITS transfira todos os arquivos no trabalho. Nesse ponto, o trabalho passa para o estado transferido. O BITS usa agendamento Round Robin para agendar trabalhos que estão no mesmo nível de prioridade. Cada trabalho recebe uma fatia de tempo para processar seus arquivos. Se o trabalho não for concluído durante sua fração de tempo, o trabalho volta para o estado enfileirado e o próximo trabalho na fila é ativado. Isso impede que trabalhos grandes bloqueiem trabalhos menores. Os trabalhos são processados amplamente em uma base PEPS (primeiro a entrar, primeiro a sair); no entanto, o BITS não pode garantir o processamento de FIFO devido a agendamento de Round-Robin, erros de trabalho e reinicializações de serviço.

Os arquivos transferidos não estão disponíveis para o cliente até que o aplicativo chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) para transferir a propriedade dos arquivos de bits para o usuário. Os trabalhos de upload também são definidos para o estado transferido quando o arquivo é recebido com êxito pelo servidor. Os trabalhos de resposta de upload são definidos para o estado transferido depois que o arquivo é enviado com êxito ao servidor e a resposta do aplicativo de servidor é transferida com êxito para o cliente.

Se ocorrer um erro, o trabalho será movido para o estado de erro fatal ou transitório. Erros fatais são erros dos quais o BITS não pode se recuperar ou que exigem a correção da intervenção. Se o aplicativo for capaz de corrigir o erro, o aplicativo retoma o trabalho e os BITS movem o trabalho para o estado na fila. Erros transitórios são erros que podem ser resolvidos por conta própria. O BITS tenta novamente trabalhos no estado de erro transitório até que a transferência seja bem-sucedida ou o trabalho expire. O trabalho atinge o tempo limite quando nenhum progresso é feito dentro de um período especificado pelo aplicativo. Se o trabalho atingir o tempo limite, o BITS moverá o trabalho para o estado de erro fatal.

Para saber mais sobre os Estados de trabalho, confira [**BG \_ \_ estado do trabalho**](/windows/desktop/api/Bits/ne-bits-bg_job_state).
