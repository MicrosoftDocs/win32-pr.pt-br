---
title: Sobre o DDEML
description: Este tópico discute a troca dinâmica de dados.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Interface do Usuário,Dados Dinâmicos Exchange (DDE)
- Dados Dinâmicos Exchange (DDE), sobre
- DDE (Dados Dinâmicos Exchange),sobre
- troca de dados, Dados Dinâmicos Exchange (DDE)
- Windows Interface do Usuário,Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados Dinâmicos Exchange)
- Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange), sobre
- DDEML (biblioteca Dados Dinâmicos Exchange gerenciamento de dados),sobre
- troca de dados, Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados)
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

Dados Dinâmicos Exchange (DDE) difere do mecanismo de transferência de dados da área de transferência. Uma diferença é que a área de transferência quase sempre é usada como uma resposta única para uma ação específica pelo usuário , como clicar em **Colar** em um menu. Embora o DDE também possa ser iniciado por um usuário, ele normalmente continua sem o envolvimento do usuário.

A Dados Dinâmicos Exchange DDEML fornece uma interface que simplifica a tarefa de adicionar a funcionalidade DDE a um aplicativo. Em vez de enviar, postar e processar mensagens DDE diretamente, um aplicativo usa as funções fornecidas pelo DDEML para gerenciar conversas DDE. Uma conversa de DDE é a interação entre aplicativos cliente e servidor. O DDEML também fornece um meio para gerenciar as cadeias de caracteres e os dados compartilhados entre aplicativos DDE. Em vez de usar átomos e ponteiros para objetos de memória compartilhados, os aplicativos DDE criam e trocam identificador de cadeia de caracteres, que identificam cadeias de caracteres e identificador de dados, que identificam objetos DDE. O DDEML fornece uma função ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite que um aplicativo de servidor registre os nomes de serviço com suporte. Os nomes de serviço são então transmitidos para outros aplicativos no sistema, que usam os nomes para se conectar ao servidor. O DDEML também garante a compatibilidade entre aplicativos DDE exigindo que eles implementem o protocolo DDE de maneira consistente.

Os aplicativos existentes que usam o protocolo DDE baseado em mensagem são totalmente compatíveis com aqueles que usam o DDEML; ou seja, um aplicativo que usa dDE baseado em mensagem pode estabelecer conversas e executar transações com aplicativos usando o DDEML. Em vez de usar mensagens DDE em seu novo aplicativo, aproveite o DDEML e as muitas melhorias que ele oferece.

Para usar o DDEML, você deve incluir o DDEML. Arquivo de título H em seus arquivos de origem, vincule com USER32. Arquivo LIB e certifique-se de que DDEML.DLL arquivo de segurança reside no caminho do sistema.

Sempre que uma função DDEML falha, um aplicativo pode chamar a [**função DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar a causa da falha. **DdeGetLastError** retorna um valor de erro que especifica a causa do erro mais recente.

 

 




