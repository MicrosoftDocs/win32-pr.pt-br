---
title: Sobre o DDEML
description: Este tópico discute a troca de dados dinâmicas.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Interface do usuário, troca dinâmica de dados (DDE)
- troca dinâmica de dados (DDE), sobre
- DDE (troca dinâmica de dados), sobre
- troca de dados, troca dinâmica de dados (DDE)
- Windows Interface do usuário, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- biblioteca de gerenciamento de troca dinâmica de dados (DDEML), sobre
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), sobre
- data exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d4efea534918ac3fd3da46364e3cb528e4199498ea7533c1635af6780cc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545557"
---
# <a name="about-the-ddeml"></a>Sobre o DDEML

o troca dinâmica de dados (DDE) difere do mecanismo de transferência de dados da área de transferência. Uma diferença é que a área de transferência é quase sempre usada como uma resposta única para uma ação específica pelo usuário, como clicar em **colar** em um menu. Embora o DDE também possa ser iniciado por um usuário, ele normalmente continua sem o envolvimento adicional do usuário.

a biblioteca de gerenciamento de troca dinâmica de dados (DDEML) fornece uma interface que simplifica a tarefa de adicionar capacidade DDE a um aplicativo. Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE. Uma conversa DDE é a interação entre aplicativos cliente e servidor. O DDEML também fornece um meio para gerenciar as cadeias de caracteres e os dados compartilhados entre aplicativos DDE. Em vez de usar Atoms e ponteiros para objetos de memória compartilhados, os aplicativos DDE criam e trocam identificadores de cadeias de caracteres, que identificam cadeias e identificadores de dados, que identificam objetos DDE. O DDEML fornece uma função ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite que um aplicativo de servidor registre os nomes de serviço com suporte. Os nomes de serviço são então difundidos para outros aplicativos no sistema, que usam os nomes para se conectar ao servidor. O DDEML também garante a compatibilidade entre aplicativos DDE, exigindo que eles implementem o protocolo DDE de maneira consistente.

Os aplicativos existentes que usam o protocolo DDE baseado em mensagem são totalmente compatíveis com aqueles que usam o DDEML; ou seja, um aplicativo que usa o DDE baseado em mensagem pode estabelecer conversas e executar transações com aplicativos usando o DDEML. Em vez de usar mensagens DDE em seu novo aplicativo, aproveite o DDEML e os vários aprimoramentos que ele oferece.

Para usar o DDEML, você deve incluir o DDEML. Arquivo de cabeçalho H em seus arquivos de origem, vincule com o USER32. LIB e verifique se o arquivo de DDEML.DLL reside no caminho do sistema.

Sempre que uma função DDEML falha, um aplicativo pode chamar a função [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar a causa da falha. **DdeGetLastError** retorna um valor de erro que especifica a causa do erro mais recente.

 

 




