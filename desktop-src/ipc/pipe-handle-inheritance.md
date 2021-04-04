---
description: O servidor de pipe controla se seus identificadores podem ser herdados das seguintes maneiras.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Herança de identificador de pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646692"
---
# <a name="pipe-handle-inheritance"></a>Herança de identificador de pipe

O servidor de pipe controla se seus identificadores podem ser herdados das seguintes maneiras:

-   A função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) recebe uma estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Se o servidor de pipe definir o membro **bInheritHandle** dessa estrutura como **true**, os identificadores criados por **CreatePipe** poderão ser herdados.
-   O servidor de pipe pode usar a função [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) para alterar a herança de um identificador de pipe. O servidor de pipe pode criar uma duplicata não hereditária de um identificador de pipe herdável ou uma duplicata herdável de um identificador de pipe não herdado.
-   A função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) permite que o servidor de pipe especifique se um processo filho herda todos ou nenhum de seus identificadores herdáveis.

Quando um processo filho herda um identificador de pipe, o sistema permite que o processo acesse o pipe. No entanto, o processo pai deve comunicar o valor do identificador ao processo filho. O processo pai geralmente faz isso redirecionando o identificador de saída padrão para o processo filho, conforme mostrado nas etapas a seguir:

1.  Chame a função [**GetStdHandle**](/windows/console/getstdhandle) para obter a alça de saída padrão atual; Salve esse identificador para que você possa restaurar o identificador de saída padrão original depois que o processo filho tiver sido criado.
2.  Chame a função [**SetStdHandle**](/windows/console/setstdhandle) para definir o identificador de saída padrão para o identificador de gravação no pipe. Agora, o processo pai pode criar o processo filho.
3.  Chame a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para fechar o identificador de gravação no pipe. Depois que o processo filho herda o identificador de gravação, o processo pai não precisa mais de sua cópia.
4.  Chame [**SetStdHandle**](/windows/console/setstdhandle) para restaurar o identificador de saída padrão original.

O processo filho usa a função [**GetStdHandle**](/windows/console/getstdhandle) para obter seu identificador de saída padrão, que agora é um identificador para a extremidade de gravação de um pipe. Em seguida, o processo filho usa a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar sua saída para o pipe. Quando o filho termina com o pipe, ele deve fechar o identificador de pipe chamando [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) ou encerrando, o que fecha automaticamente o identificador.

O processo pai usa a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para receber a entrada do pipe. Os dados são gravados em um pipe anônimo como um fluxo de bytes. Isso significa que o processo pai de leitura de um pipe não pode distinguir entre os bytes gravados em operações de gravação separadas, a menos que os processos pai e filho usem um protocolo para indicar onde a operação de gravação termina. Quando todos os identificadores de gravação para o pipe são fechados, a função **ReadFile** retorna zero. É importante que o processo pai Feche seu identificador para a extremidade de gravação do pipe antes de chamar **ReadFile**. Se isso não for feito, a operação **ReadFile** não poderá retornar zero porque o processo pai tem um identificador aberto para a extremidade de gravação do pipe.

O procedimento para redirecionar o identificador de entrada padrão é semelhante ao de redirecionar o identificador de saída padrão, exceto que o identificador de leitura do pipe é usado como o identificador de entrada padrão do filho. Nesse caso, o processo pai deve garantir que o processo filho não herde o identificador de gravação do pipe. Se isso não for feito, a operação [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) executada pelo processo filho não poderá retornar zero porque o processo filho tem um identificador aberto para a extremidade de gravação do pipe.

Para um programa de exemplo que usa Pipes anônimos para redirecionar os identificadores padrão de um processo filho, consulte [criando um processo filho com entrada e saída redirecionadas](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
