---
description: Descreve os bloqueios oportunistas de nível 1, nível 2, lote e filtro.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Tipos de bloqueios oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a755a6ff766f5d19e13d4b269c1ba4bb9803e934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829675"
---
# <a name="types-of-opportunistic-locks"></a>Tipos de bloqueios oportunistas

As operações de bloqueio oportunista funcionam com quatro tipos de bloqueios oportunistas: nível 1, nível 2, lote e filtro. *Bloqueios oportunistas exclusivos* são bloqueios de nível 1, lote e filtro. Se um thread tiver qualquer tipo de bloqueio exclusivo em um arquivo, ele também não poderá ter um bloqueio de nível 2 no mesmo arquivo.

## <a name="level-1-opportunistic-locks"></a>Bloqueios oportunistas de nível 1

Um bloqueio oportunista de nível 1 em um arquivo permite que um cliente leia a frente no arquivo e armazene em cache o Read-Ahead e grave dados do arquivo localmente. Desde que o cliente tenha acesso exclusivo a um arquivo, não há nenhum risco de coerência de dados ao fornecer um bloqueio oportunista de nível 1.

O cliente pode solicitar um bloqueio oportunista de nível 1 depois de abrir um arquivo. Se nenhum outro cliente (ou nenhum outro thread no mesmo cliente) tiver o arquivo aberto, o servidor poderá conceder o bloqueio oportunista. Em seguida, o cliente pode armazenar em cache a leitura e gravação de dados do arquivo localmente. Se outro cliente tiver aberto o arquivo, o servidor recusará o bloqueio oportunista e o cliente não fará cache local. (O servidor pode recusar o bloqueio oportunista por outros motivos também, como não oferecer suporte a bloqueios oportunistas.)

Quando o servidor abre um arquivo que já tem um bloqueio oportunista de nível 1, o servidor examina o estado de compartilhamento do arquivo antes de interromper o bloqueio oportunista de nível 1. Se o servidor interromper o bloqueio após esse exame, o tempo que o cliente com o bloqueio anterior passa a liberar seu cache de gravação é o tempo que o cliente solicita que o arquivo deve aguardar. Esse período de despesas significa que os bloqueios oportunistas de nível 1 devem ser evitados em arquivos que muitos clientes abrem.

No entanto, como o servidor verifica o estado de compartilhamento antes de interromper o bloqueio, no caso em que o servidor negaria uma solicitação aberta devido a um conflito de compartilhamento, o servidor não interrompe o bloqueio. Por exemplo, se você tiver aberto um arquivo, o compartilhamento negado para operações de gravação e obtido um bloqueio de nível 1, o servidor negará a solicitação de outro cliente para abrir o arquivo para gravação antes que ele examine o bloqueio no arquivo. Nessa instância, o bloqueio oportunista não é interrompido.

Para obter um exemplo de como um bloqueio oportunista de nível 1 funciona, consulte exemplo de bloqueio oportunista de nível 1. Para saber mais sobre como interromper os bloqueios oportunistas, confira [bloqueios oportunistas](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Bloqueios oportunistas de nível 2

Um bloqueio oportunista de nível 2 informa um cliente de que há vários clientes simultâneos de um arquivo e que nenhum ainda o modificou. Esse bloqueio permite que o cliente execute operações de leitura e obtenha atributos de arquivo usando informações locais em cache ou de leitura antecipada, mas o cliente deve enviar todas as outras solicitações (como para operações de gravação) para o servidor. Seu aplicativo deve usar o bloqueio oportunista de nível 2 quando você espera que outros aplicativos gravem no arquivo aleatoriamente ou leiam o arquivo aleatoriamente ou sequencialmente.

Um bloqueio oportunista de nível 2 é muito semelhante a um bloqueio oportunista de filtro. Na maioria das situações, seu aplicativo deve usar o bloqueio oportunista de nível 2. Somente use o bloqueio de filtro se você não quiser que as operações abertas para leitura causem violações no modo de compartilhamento no período de tempo entre o aplicativo que está abrindo o arquivo e recebendo o bloqueio. Para obter mais informações, consulte filtrar bloqueios oportunistas e [resposta do servidor para abrir solicitações em arquivos bloqueados](server-response-to-open-requests-on-locked-files.md).

Para saber mais sobre como interromper os bloqueios oportunistas, confira [bloqueios oportunistas](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Bloqueios oportunistas em lote

Um bloqueio oportunista em lote manipula aberturas e fechamentos de arquivos. Por exemplo, na execução de um arquivo em lotes, o arquivo em lotes pode ser aberto e fechado uma vez para cada linha do arquivo. Um bloqueio oportunista em lote abre o arquivo em lotes no servidor e o mantém aberto. Como o processador de comando "abre" e "fecha" o arquivo em lotes, o redirecionador de rede intercepta os comandos abrir e fechar. Todo o servidor recebe os comandos de busca e leitura. Se o cliente também estiver lendo com antecedência, o servidor receberá uma solicitação de leitura específica no máximo uma vez.

Ao abrir um arquivo que já tem um bloqueio oportunista em lote, o servidor verifica o estado de compartilhamento do arquivo depois de interromper o bloqueio. Essa verificação fornece ao proprietário do bloqueio a chance de concluir a liberação de seu cache e fechar o identificador de arquivo. Uma operação aberta tentada durante a verificação de compartilhamento não faz com que a verificação de compartilhamento falhe se o proprietário do bloqueio liberar o bloqueio.

Para obter um exemplo de como funciona um bloqueio oportunista em lotes, consulte exemplo de bloqueio oportunista em lote. Para saber mais sobre como interromper os bloqueios oportunistas, confira [bloqueios oportunistas](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtrar bloqueios oportunistas

Um bloqueio oportunista de filtro bloqueia um arquivo para que ele não possa ser aberto para o acesso de gravação ou exclusão. Todos os clientes devem ser capazes de compartilhar o arquivo. Os bloqueios de filtro permitem que os aplicativos executem operações de filtragem não intrusivas em dados de arquivo (por exemplo, um compilador abrindo código-fonte ou um programa de catalogação).

Um bloqueio oportunista de filtro difere de um bloqueio oportunista de nível 2, pois permite que operações abertas para leitura ocorram sem violações de modo de compartilhamento no período de tempo entre o aplicativo que está abrindo o arquivo e recebendo o bloqueio. O bloqueio oportunista de filtro é o melhor bloqueio a ser usado quando for importante permitir que outros clientes leiam o acesso. Em outros casos, seu aplicativo deve usar um bloqueio oportunista de nível 2. Um bloqueio oportunista de filtro difere de um bloqueio oportunista em lote, pois ele não permite que várias aberturas e fechamentos sejam tratados pelo redirecionador de rede como faz um bloqueio oportunista em lote.

Seu aplicativo deve solicitar um bloqueio oportunista de filtro em um arquivo em três etapas:

1.  Use a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir um identificador para o arquivo com o parâmetro *desiredAccess* definido como zero, indicando que não há acesso e o parâmetro *dwShareMode* definido como o sinalizador de **\_ \_ leitura de compartilhamento de arquivos** para permitir o compartilhamento para leitura. O identificador obtido nesse ponto é chamado de identificador de bloqueio.
2.  Solicite um bloqueio nesse identificador com o código de controle [**\_ oplock do \_ filtro \_ de solicitação fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) .
3.  Quando o bloqueio for concedido, use [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir o arquivo novamente com *desiredAccess* definido como o sinalizador de **\_ leitura genérico** . Defina *dwShareMode* como o sinalizador de **\_ \_ leitura de compartilhamento de arquivos** para permitir que outras pessoas leiam o arquivo enquanto você o tiver aberto, o sinalizador de **\_ \_ exclusão de compartilhamento de arquivos** para permitir que outras pessoas marquem o arquivo para exclusão enquanto você o tiver aberto, ou ambos. O identificador obtido nesse ponto é chamado de identificador de leitura.

Use a alça de leitura para ler ou gravar o conteúdo do arquivo.

Ao abrir um arquivo que já tem um filtro de bloqueio oportunista, o servidor interrompe o bloqueio e verifica o estado de compartilhamento do arquivo. Essa verificação fornece ao cliente que mantinha o bloqueio oportunista anterior a chance de abandonar todos os dados armazenados em cache e confirmar a interrupção. Uma operação aberta tentada durante essa verificação de compartilhamento não faz com que a verificação de compartilhamento falhe se o antigo proprietário do bloqueio liberar o bloqueio. O sistema de arquivos mantém em abeyance a operação de abertura até que o proprietário do bloqueio feche a alça de leitura e, em seguida, a alça de bloqueio. Depois que isso for feito, a solicitação aberta do outro cliente poderá continuar.

Para saber mais sobre como interromper os bloqueios oportunistas, confira [bloqueios oportunistas](breaking-opportunistic-locks.md).

 

 
