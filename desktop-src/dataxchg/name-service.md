---
title: Serviço de nome
description: Este tópico discute como a biblioteca de gerenciamento de troca dinâmica de dados possibilita que um aplicativo de servidor registre os nomes de serviço aos quais ele dá suporte.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Interface do usuário do Windows, troca dinâmica de dados (DDE)
- Troca dinâmica de dados (DDE), serviço de nome
- DDE (troca dinâmica de dados), serviço de nome
- troca de dados, troca dinâmica de dados (DDE)
- Interface do usuário do Windows, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), serviço de nome
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), serviço de nome
- Data Exchange, biblioteca de gerenciamento de troca dinâmica de dados (DDEML)
- Troca dinâmica de dados (DDE), registro de nome de serviço
- DDE (troca dinâmica de dados), registro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), registro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), registro de nome de serviço
- Troca dinâmica de dados (DDE), filtro de nome de serviço
- DDE (troca dinâmica de dados), filtro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), filtro de nome de serviço
- DDEML (biblioteca de gerenciamento de troca dinâmica de dados), filtro de nome de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292846"
---
# <a name="name-service"></a>Serviço de nome

A biblioteca de gerenciamento de troca dinâmica de dados (DDEML) possibilita que um aplicativo de servidor registre os nomes de serviço aos quais ele dá suporte e impeça que o DDEML envie transações de [**\_ conexão XTYP**](xtyp-connect.md) para nomes de serviço sem suporte na função de retorno de chamada do troca dinâmica de dados (DDE) do servidor.

Os tópicos a seguir descrevem o nome do serviço.

-   [Registro de nome de serviço](#service-name-registration)
-   [Filtro de nome de serviço](#service-name-filter)

## <a name="service-name-registration"></a>Registro de nome de serviço

Ao registrar seus nomes de serviço com o DDEML, um servidor informa outros aplicativos DDE no sistema que um novo servidor está disponível. Um servidor registra um nome de serviço chamando a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) e especificando um identificador de cadeia de caracteres que identifica o nome. Em resposta, o DDEML envia uma transação de [**\_ registro de XTYP**](xtyp-register.md) para a função de retorno de chamada de cada aplicativo ddeml no sistema (exceto aqueles que especificavam o \_ sinalizador de filtro CBF ignorar \_ registros na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ). A transação de **\_ registro XTYP** passa dois identificadores de cadeia de caracteres para uma função de retorno de chamada: o primeiro identifica a cadeia de caracteres que especifica o nome do serviço base e o segundo identifica a cadeia de caracteres que especifica o serviço específico da instância. Um cliente geralmente usa o nome do serviço base em uma lista de servidores disponíveis, para que o usuário possa selecionar um servidor na lista. O cliente usa o nome de serviço específico da instância para estabelecer uma conversa com uma instância específica de um aplicativo de servidor, se mais de uma instância estiver em execução.

Um servidor pode usar [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para cancelar o registro de um nome de serviço. Essa função faz com que o DDEML envie [**XTYP o \_ registro**](xtyp-unregister.md) de transações para os outros aplicativos DDE no sistema, informando que eles não podem mais usar o nome para estabelecer conversas.

Um servidor deve chamar [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar seus nomes de serviço logo após chamar [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Um servidor deve cancelar o registro de seus nomes de serviço usando **DdeNameService** logo antes de chamar a função [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .

## <a name="service-name-filter"></a>Filtro de nome de serviço

Além de registrar nomes de serviço, o [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) habilita um servidor a ativar ou desativar seu filtro de nome de serviço. Quando um servidor desativa seu filtro de nome de serviço, o DDEML envia a transação [**XTYP \_ Connect**](xtyp-connect.md) para a função de retorno de chamada DDE do servidor sempre que qualquer cliente chama a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , independentemente do nome do serviço especificado na função. Quando um servidor ativa seu filtro de nome de serviço, o DDEML envia a transação **XTYP \_ Connect** para o servidor somente quando **DdeConnect** especifica um nome de serviço que o servidor especificou em uma chamada para **DdeNameService**.

Por padrão, o filtro de nome de serviço está ativado quando um aplicativo chama [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Esse padrão impede que o DDEML envie a transação [**XTYP \_ Connect**](xtyp-connect.md) para um servidor antes que o servidor tenha criado a cadeia de caracteres necessária. Um servidor pode desativar seu filtro de nome de serviço especificando o \_ sinalizador DNS FILTEROFF em uma chamada para [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). O \_ sinalizador de filtragem DNS ativa o filtro.

 

 




