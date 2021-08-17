---
description: Operações de pipe anônimo, incluindo criação de pipe, gravação em um pipe, identificadores de pipe.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Operações de pipe anônimo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4c684daab5dd1c18dbf5eb22e2191f193e7ecc3b088ac58e3f680f442897a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350706"
---
# <a name="anonymous-pipe-operations"></a>Operações de pipe anônimo

A função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) cria um pipe anônimo e retorna dois identificadores: um identificador de leitura para o pipe e um identificador de gravação para o pipe. O identificador de leitura tem acesso somente leitura ao pipe e o identificador de gravação tem acesso somente gravação ao pipe. Para se comunicar usando o pipe, o servidor de pipe deve passar um identificador de pipe para outro processo. Normalmente, isso é feito por meio de herança; ou seja, o processo permite que o identificador seja herdado por um processo filho. O processo também pode duplicar um identificador de pipe usando a função [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) e enviá-lo para um processo não relacionado usando alguma forma de comunicação entre processos, como DDE ou memória compartilhada.

Um servidor de pipe pode enviar a alça de leitura ou o identificador de gravação para o cliente de pipe, dependendo se o cliente deve usar o pipe anônimo para enviar informações ou receber informações. Para ler a partir do pipe, use o identificador de leitura do pipe em uma chamada para a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . A chamada **ReadFile** retorna quando outro processo foi gravado no pipe. A chamada **ReadFile** também pode retornar se todos os identificadores de gravação no pipe tiverem sido fechados ou se um erro ocorrer antes da operação de leitura ser concluída.

Para gravar no pipe, use o identificador de gravação do pipe em uma chamada para a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) . A chamada **WriteFile** não retorna até que tenha gravado o número especificado de bytes no pipe ou um erro ocorra. Se o buffer de pipe estiver cheio e houver mais bytes a serem gravados, **WriteFile** não retornará até que outro processo Leia a partir do pipe, disponibilizando mais espaço em buffer. O servidor de pipe especifica o tamanho do buffer para o pipe quando ele chama [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe).

Não há suporte para operações de leitura e gravação assíncronas (sobrepostas) em Pipes anônimos. Isso significa que você não pode usar as funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) com Pipes anônimos. Além disso, o parâmetro *lpOverlapped* de [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) é ignorado quando essas funções são usadas com Pipes anônimos.

Um pipe anônimo existe até que todos os identificadores de pipe, leitura e gravação, tenham sido fechados. Um processo pode fechar seus identificadores de pipe usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Todos os identificadores de pipe também são fechados quando o processo é encerrado.

Os pipes anônimos são implementados usando um pipe nomeado com um nome exclusivo. Portanto, muitas vezes você pode passar um identificador para um pipe anônimo para uma função que requer um identificador para um pipe nomeado.

 

 
