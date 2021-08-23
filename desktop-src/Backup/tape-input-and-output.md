---
title: Entrada e saída de fita
description: Há várias funções que os aplicativos podem usar para executar entrada e saída (e/s) em uma unidade de fita. E/s de fita é semelhante à e/s executada em um dispositivo de comunicações.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Backup de entrada e saída de fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281eb6104cb71fbd5e7f0b3d9072cefe562ac7b9cc54e05ede53bece8755178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021264"
---
# <a name="tape-input-and-output"></a>Entrada e saída de fita

Há várias funções que os aplicativos podem usar para executar entrada e saída (e/s) em uma unidade de fita. E/s de fita é semelhante à e/s executada em um dispositivo de comunicações.

Ao executar a e/s de fita, algumas unidades de fita armazenam informações de firmware de fita nos primeiros blocos em uma fita, normalmente usando alguma parte dos primeiros 100 blocos. Os aplicativos não devem usar esses blocos. Informações mais específicas sobre esse assunto estão disponíveis em fabricantes de sistemas de fita individuais. Em geral, um aplicativo que ignora os primeiros 100 blocos em uma fita evitará idiossincrasias de unidade de fita.

As funções [**GetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) e [**SetTapePosition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) recuperam e movem a posição da fita atual. A função [**WriteTapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) grava um número especificado de marcações, marcas de gravação, marcas de gravação curtas e longas marcas de filemarcações. A função [**EraseTape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) apaga toda ou parte de uma fita.

As funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) lêem e gravam dados de arquivo de e para a fita. Os dados são lidos e gravados em blocos completos. Se o tamanho do bloco da fita for 512 bytes, todas as operações de leitura e gravação deverão usar buffers que sejam múltiplos inteiros simples desse tamanho de bloco: 512, 1024, 1536, 2048 e assim por diante. A maioria, se não todas, as unidades só permitem uma operação de gravação depois que a fita é rebobinada ou depois que uma operação de leitura produz uma mensagem de erro de fim de dados.

Para ler ou gravar dados de arquivo de ou para uma fita em modo de bloco de comprimento variável, execute as seguintes etapas:

1.  Determine se a unidade de fita dá suporte ao modo de bloco de comprimento variável chamando a função [**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) e verificando o \_ \_ bit do bloco variável da unidade de fita \_ do membro **FeaturesLow** da estrutura de [**\_ obter \_ \_ parâmetros da unidade de fita**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) retornada.
2.  Especifique o modo de tamanho do bloco variável chamando a função [**Settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) , definindo o membro **BlockSize** da estrutura de parâmetros de mídia do conjunto de fitas como zero. [**\_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) Em seguida, use [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para ler ou gravar os dados do arquivo.

Se o [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) encontrar uma marca de um, os dados até a marca de filemark serão lidos e a função falhará. (A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um código de erro que indica o tipo de marca de texto que foi encontrado.) O sistema operacional move a fita além da marca de caixa de mensagem e um aplicativo pode chamar **ReadFile** novamente para continuar lendo.

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) lêem e gravam apenas o fluxo de dados. As funções [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) lêem e gravam todos os fluxos associados a um arquivo. Isso inclui dados, atributos estendidos, segurança e fluxos de dados alternativos. Os fluxos de dados de segurança e alternativos são relevantes apenas na partição do sistema de arquivos NTFS.

A função [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) busca adiante em um arquivo inicialmente acessado por [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) ou [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite). Essa função permite que um aplicativo ignore informações que causam erros de acesso.

Se um aplicativo precisar acessar apenas os dados do arquivo, ele deverá usar [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Essas funções também podem ler fluxos de dados alternativos se os fluxos foram criados usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

Um aplicativo de backup em fita deve usar [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) e [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) para copiar todas as informações pertencentes a um arquivo. No entanto, essas funções não lêem ou gravam características do arquivo, como atributos, hora de criação do arquivo e assim por diante. Os aplicativos devem usar as funções de entrada e saída de arquivo, como [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) e [**SetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), para recuperar e definir esses valores.

 

 