---
description: Ao usar CSPs de provedores de serviço de criptografia, tenha em mente as convenções a seguir.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Usando CSPs: processos gerais'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784138"
---
# <a name="using-csps-general-processes"></a>Usando CSPs: processos gerais

Ao usar CSPs de [*provedores de serviço de criptografia*](../secgloss/c-gly.md) , tenha em mente as convenções a seguir.

## <a name="private-key-caching"></a>Cache de chave privada

Um CSP pode armazenar em cache algumas [*chaves privadas*](../secgloss/p-gly.md). É possível controlar esse cache de chave privada em um global, mas não em um aplicativo específico. As alterações de cache são feitas modificando determinadas configurações do registro. Para obter mais informações, consulte [**constantes de cache de chave privada**](private-key-caching-constants.md).

## <a name="example-code-conventions"></a>Convenções de código de exemplo

Para fornecer um código mais conciso e mais legível, alguns princípios da boa prática de programação nem sempre são seguidos nos exemplos. Especialmente:

-   Somente respostas de erro limitadas são mostradas. Bem-escrito, os programas completos verificam os códigos de erro e executam as ações apropriadas quando um erro é encontrado.
-   Somente a memória limitada e o gerenciamento de recursos são feitos. Bem-escrito, programas completos destrói todas as chaves e [*hashes*](../secgloss/h-gly.md), liberam toda a memória alocada, fecham todos os arquivos e liberam todos os identificadores. Esses exemplos fornecem apenas demonstrações limitadas do uso de funções que executam essas tarefas. Esses exemplos não executam nenhuma tarefa de gerenciamento de recursos ou memória no caso de encerramento do programa devido a erros.

Os tópicos a seguir apresentam informações gerais sobre exemplos de procedimento, bem como código de exemplo.

-   [Recuperando dados de comprimento desconhecido](retrieving-data-of-unknown-length.md)
-   [Enumerando protocolos com suporte](enumerating-supported-protocols.md)

 

 
