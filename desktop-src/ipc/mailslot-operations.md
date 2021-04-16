---
description: Descrições das funções a serem usadas ao trabalhar com processadores de execução, clientes e servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operações de processador de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0055ad434971659dc2cfd058146029bb63023654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772513"
---
# <a name="mailslot-operations"></a>Operações de processador de processadores

Ao trabalhar com processadores de execução, os clientes e servidores devem usar apenas as funções discutidas nas tabelas a seguir. Não use outras funções, mesmo que aceitem identificadores de arquivo ou nomes de arquivo como parâmetros, pois eles não são projetados para trabalhar com processadores de arquivos.

## <a name="mailslot-server-functions"></a>Funções do servidor do processador de processadores

Os servidores de processador de processadores têm uso exclusivo de três funções, conforme mostrado na tabela a seguir.



| Função                                   | Descrição                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Cria um processador de processadores e retorna um identificador de processador de processadores.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera o tamanho máximo da mensagem, o tamanho do processador de mensagens, o tamanho da próxima mensagem no processador de itens, o número de emails no processador e a quantidade de tempo que uma operação de leitura pode esperar por uma mensagem. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Altera o tempo limite de leitura para um processador de itens.                                                                                                                                                                    |



 

As funções a seguir também são usadas por servidores do processador de processadores.



| Função                                                         | Descrição                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica o identificador do processador de processadores.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera mensagens de um processador de mensagem.                 |
| [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera a data e a hora em que um processador de processadores foi criado. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Define a data e a hora em que um processador de linhas foi criado.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera as propriedades do identificador do processador de processadores.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Define as propriedades do identificador do processador de linhas.             |



 

## <a name="mailslot-client-functions"></a>Funções de cliente do processador de processadores

Um processo de cliente usa as funções a seguir ao interagir com um processador de processadores.



| Função                                                             | Descrição                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Fecha um identificador de processador de processadores para um processo de cliente.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Cria um identificador de processador de processadores para um processo de cliente. |
| [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica um identificador de processador de processadores.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Grava dados em um processador de processadores.                      |



 

 

 
