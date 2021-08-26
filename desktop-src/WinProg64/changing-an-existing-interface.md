---
title: Alterando uma interface existente
description: Sempre que possível, implemente uma nova interface para seu aplicativo, em vez de fazer alterações em uma existente.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- alterando as interfaces existentes de 64 bits Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782587471de5616750501552445599a94571ff2275d080347937c595e2cd7668
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899066"
---
# <a name="changing-an-existing-interface"></a>Alterando uma interface existente

Sempre que possível, implemente uma nova interface para seu aplicativo, em vez de fazer alterações em uma existente. Se não for possível evitar a alteração de uma interface existente, use novos tipos de dados somente em novos métodos. A introdução de um novo tipo de dados ou a modificação de um tipo existente é a fonte mais comum de problemas de incompatibilidade. O modelo de tempo de execução RPC pressupõe que o aplicativo de recebimento sabe sobre os tipos de dados que recebe, de modo que os dados são colocados na conexão sem uma descrição de dados genéricos. Quando o destinatário espera um tipo de dados diferente daquele que o remetente colocou na conexão, o stub gera uma exceção (ou a transmissão falha de alguma outra maneira menos amigável).

Uma interface RPC é definida por seu UUID e seus números de versão principal e secundária. Ao alterar uma interface existente, você deve adicionar os novos métodos no final da interface e alterar o número de versão secundária. Se você adicionar métodos em qualquer outro lugar ou fizer outras alterações na interface, também será necessário alterar o número de versão principal.

Na verdade, há ocasiões em que não é possível alterar até mesmo o número de versão secundária, pois um novo cliente não poderá se comunicar com um servidor antigo e você não poderá atualizar o servidor. O tempo de execução de RPC gera uma exceção, RPC \_ S \_ PROCNUM \_ fora \_ do \_ intervalo, quando um cliente chama um método além daqueles especificados para sua interface com o servidor. A solução alternativa é deixar os números de versão inalterados e escrever seu código de cliente para tratar essa exceção normalmente – pelo cliente degradando seu desempenho, por exemplo, ou por qualquer meio que seja apropriado para seu aplicativo.

Há uma solução alternativa semelhante para um caso especial de alteração de um tipo de dados em um método existente. Se você tiver uma [**União**](/windows/desktop/Midl/union) cujas ramificações são ponteiros e que não têm uma ramificação padrão para tipos não reconhecidos, você pode adicionar um novo Branch que usa o novo tipo de dados. Isso não alterará o tamanho da estrutura de dados. Quando o cliente se comunica com um novo servidor, ele pode usar o novo tipo de dados. No entanto, quando o cliente se comunica com um servidor antigo, o tempo de execução irá gerar a exceção RPC \_ S \_ Invalid \_ . Novamente, você precisará escrever seu código de cliente para tratar essa exceção adequadamente.

Uma interface DCOM é identificada por seu GUID. No DCOM, as interfaces são consideradas imutáveis e você só pode fazer alterações criando uma nova interface que herda da antiga. Essas regras garantem que os clientes e servidores permaneçam compatíveis.

 

 