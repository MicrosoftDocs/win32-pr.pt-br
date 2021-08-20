---
description: Ao usar CSPs de provedores de serviços criptográficos, tenha em mente as convenções a seguir.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Usando CSPs: Processos Gerais'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d812e5a70b6df664247a92ec957808c87b7328d18d41d2fb88b3b4fd78f2c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971557"
---
# <a name="using-csps-general-processes"></a>Usando CSPs: Processos Gerais

Ao usar [*CSPs de provedores de serviços criptográficos,*](../secgloss/c-gly.md) tenha em mente as convenções a seguir.

## <a name="private-key-caching"></a>Chave privada Caching

Um CSP pode armazenar algumas [*chaves privadas em cache.*](../secgloss/p-gly.md) É possível controlar esse cache de chave privada em uma base global, mas não específica do aplicativo. Caching alterações são feitas modificando determinadas configurações do Registro. Para obter mais informações, [**consulte Private Key Caching Constants**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Convenções de código de exemplo

Para fornecer um código mais conciso e acessível, alguns princípios de boa prática de programação nem sempre são seguidos nos exemplos. Especialmente:

-   Somente respostas de erro limitadas são mostradas. Programas bem escritos e completos verificam os códigos de erro retornados e executam as ações apropriadas quando um erro é encontrado.
-   Somente a memória limitada e o gerenciamento de recursos são feitos. Programas bem escritos e completos destrói todas as chaves e [*hashes,*](../secgloss/h-gly.md)libera toda a memória alocada, fecha todos os arquivos e libera todos os alças. Esses exemplos fornecem apenas demonstrações limitadas do uso de funções que executam essas tarefas. Esses exemplos não executam nenhuma tarefa de gerenciamento de recursos ou memória no caso de encerramento do programa devido a erros.

Os tópicos a seguir apresentam informações gerais sobre exemplos de procedimento, bem como código de exemplo.

-   [Recuperando dados de comprimento desconhecido](retrieving-data-of-unknown-length.md)
-   [Enumerando protocolos com suporte](enumerating-supported-protocols.md)

 

 
