---
description: Representação é a capacidade de execução de um thread em um contexto de segurança diferente daquele do processo que possui o thread.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Representando um cliente de pipe nomeado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105792576"
---
# <a name="impersonating-a-named-pipe-client"></a>Representando um cliente de pipe nomeado

*Representação* é a capacidade de execução de um thread em um contexto de segurança diferente daquele do processo que possui o thread. A representação permite que o thread do servidor execute ações em nome do cliente, mas dentro dos limites do contexto de segurança do cliente. O cliente normalmente tem algum nível menor de direitos de acesso. Para obter mais informações, consulte [Impersonation](/windows/desktop/SecAuthZ/client-impersonation).

Um thread de servidor de pipe nomeado pode chamar a função [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) para assumir o token de acesso do usuário conectado à extremidade do cliente do pipe. Por exemplo, um servidor de pipe nomeado pode fornecer acesso a um banco de dados ou sistema de arquivos ao qual o servidor de pipe tem acesso privilegiado. Quando um cliente de pipe envia uma solicitação ao servidor, o servidor representa o cliente e tenta acessar o banco de dados protegido. Em seguida, o sistema concede ou nega o acesso do servidor, com base no nível de segurança do cliente. Quando o servidor for concluído, ele usará a função [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para restaurar seu token de segurança original.

O [nível de representação](/windows/desktop/SecAuthZ/impersonation-levels) determina as operações que o servidor pode executar ao representar o cliente. Por padrão, um servidor representa o nível de representação SecurityImpersonation. No entanto, quando o cliente chama a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para a extremidade do cliente do pipe, o cliente pode usar o \_ sinalizador Security SQOS \_ Present para controlar o nível de representação do servidor.

 

 
