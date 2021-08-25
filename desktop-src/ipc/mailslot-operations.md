---
description: Descrições de funções a usar ao trabalhar com emailslots, clientes e servidores.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Operações do Maillot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829496"
---
# <a name="mailslot-operations"></a>Operações do Maillot

Ao trabalhar com emailslots, os clientes e servidores devem usar apenas as funções discutidas nas tabelas a seguir. Não use outras funções, mesmo que aceitem os nomes de arquivo ou de arquivo como parâmetros, pois eles não foram projetados para trabalhar com emailslots.

## <a name="mailslot-server-functions"></a>Funções de servidor Maillot

Os servidores Maillot têm uso exclusivo de três funções, conforme mostrado na tabela a seguir.



| Função                                   | Descrição                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMailslot**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Cria um maillot e retorna um handle maillot.                                                                                                                                                            |
| [**GetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Recupera o tamanho máximo da mensagem, o tamanho do maillot, o tamanho da próxima mensagem no maillot, o número de mensagens no maillot e a quantidade de tempo que uma operação de leitura pode aguardar por uma mensagem. |
| [**SetMailslotInfo**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Altera o tempo de tempo de leitura de um maillot.                                                                                                                                                                    |



 

As funções a seguir também são usadas por servidores maillot.



| Função                                                         | Descrição                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**Duplicatehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Duplica o alça do maillot.                     |
| [**ReadFile,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [ **ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Recupera mensagens de um maillot.                 |
| [**Getfiletime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Recupera a data e a hora em que um maillot foi criado. |
| [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Define a data e a hora em que um maillot foi criado.      |
| [**GetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Recupera as propriedades do alça de maillot.        |
| [**SetHandleInformation**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Define as propriedades do alça de maillot.             |



 

## <a name="mailslot-client-functions"></a>Funções de cliente Maillot

Um processo de cliente usa as funções a seguir ao interagir com um maillot.



| Função                                                             | Descrição                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**Closehandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Fecha um handle maillot para um processo de cliente.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Cria um handle maillot para um processo de cliente. |
| [**Duplicatehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Duplica um alça de maillot.                   |
| [**WriteFile,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [ **WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Grava dados em um maillot.                      |



 

 

 
