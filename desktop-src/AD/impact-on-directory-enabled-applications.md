---
title: Impacto em aplicativos Directory-Enabled
description: Este tópico descreve o impacto em aplicativos habilitados para diretório quando ocorrem distorções de versão, atualizações parciais ou colisões.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061818fc791e1c75d440d0c477a321b8c4e5edfb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917121"
---
# <a name="impact-on-directory-enabled-applications"></a>Impacto em aplicativos Directory-Enabled

## <a name="version-skew"></a>Distorção de versão

A distorção de versão ocorre quando os aplicativos lêem os mesmos objetos de réplicas diferentes antes que uma alteração seja replicada. Os aplicativos que lêem a réplica remota reconhecem o objeto inalterado. A distorção de versão é um problema quando um determinado aplicativo ou conjunto de aplicativos usa os dados no diretório para interoperar.

Por exemplo, um serviço RPC pode publicar seus pontos de extremidade no diretório usando APIs RPC padrão (como [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta)). Os clientes se conectam ao serviço pesquisando o ponto de extremidade desejado no diretório ( [**RpcNsBindingLookupBegin**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)e assim por diante) e ligando a ele.

Suponha que um serviço RPC S ₁ publique o ponto de extremidade es ₁ e, subsequentemente, se mova para um computador diferente. O ponto de extremidade original es ₁ é alterado para E<sub>S2,</sub> refletindo o endereço do novo computador. Os clientes que lêem réplicas remotas do serviço de diretório não podem se conectar ao serviço até que o ponto de extremidade atualizado seja replicado. No entanto, mover um serviço de um computador para outro é uma ocorrência rara; Portanto, essa interrupção/atraso deve ser raramente encontrada, especialmente se a movimentação do serviço estiver bem planejada.

## <a name="partial-updates"></a>Atualizações parciais

Em geral, a atualização parcial ocorre quando um aplicativo está lendo um conjunto de dados enquanto outro aplicativo está gravando no mesmo conjunto de dados. Essa é uma situação que pode ocorrer com qualquer aplicativo em um sistema com vários mestres. Há várias maneiras que isso pode ocorrer. Você pode ter mais de um aplicativo gravando no mesmo conjunto de dados ao mesmo tempo. Se você olhar dessa forma, o serviço de replicação de diretório é apenas outro aplicativo que pode estar gravando no mesmo conjunto de dados que outro aplicativo pode estar lendo. Isso pode ser um possível problema para um aplicativo. No entanto, a janela de tempo em que uma atualização parcial pode afetar seu aplicativo é relativamente pequena. Isso raramente deve ser um problema para aplicativos que não dependem da sincronização de vários objetos. Se seu aplicativo for altamente dependente da sincronização de um conjunto de objetos relacionado, você deverá considerar os efeitos de uma atualização parcial no design do aplicativo.

Em termos de replicação de diretório, a atualização parcial ocorre quando os aplicativos lêem o mesmo conjunto de objetos de réplicas diferentes enquanto a replicação está em andamento. Os aplicativos na réplica remota veem algumas, mas não todas, as alterações.

> [!Note]  
> A janela na qual a atualização parcial pode afetar um aplicativo é pequena: o aplicativo deve começar a ler objetos enquanto a replicação de entrada está em andamento, depois que um ou mais dos objetos relacionados e alterados tiverem sido recebidos, mas antes de todos terem sido recebidos. O tempo entre as atualizações na réplica de origem afeta diretamente o tamanho dessa janela — as atualizações que ocorrem com um fechamento próximo no tempo são replicadas junto em tempo. A atualização parcial pode ser um problema quando um aplicativo usa um conjunto de objetos relacionado.

 

Por exemplo, um serviço de acesso remoto pode usar o diretório para armazenar dados de perfil e política. Os dados de política são armazenados em um conjunto de objetos e o perfil em outro conjunto. Quando um usuário se conecta ao serviço de acesso remoto, o serviço de acesso remoto lê a política para determinar se o usuário tem permissão para se conectar e se o perfil a ser aplicado à sessão do usuário. A atualização parcial pode afetar o serviço de acesso remoto de várias maneiras:

-   Se a política for complexa e consistir em vários objetos, o serviço de acesso remoto poderá ler uma política parcialmente atualizada, resultando em uma negação incorreta ou concessão de serviço ao usuário, incapacidade de processar a política devido à inconsistência interna e assim por diante.
-   Se a política e os perfis tiverem sido atualizados, o serviço poderá processar corretamente a política, mas aplicar um perfil obsoleto, pois os objetos de política foram replicados, mas os objetos de perfil não têm.
-   Se o perfil for complexo e consistir em vários objetos, o serviço poderá processar corretamente a política, mas aplicar um perfil parcialmente atualizado porque os objetos de política foram replicados, mas apenas alguns dos objetos de perfil fizeram isso.

## <a name="collisions"></a>Colisões

As colisões ocorrem quando os mesmos atributos de duas ou mais réplicas de um determinado objeto são alterados durante o mesmo intervalo de replicação. O processo de replicação reconcilia a colisão; devido à reconciliação, um usuário ou aplicativo pode "ver" um valor diferente daquele que ele escreveu.

Um exemplo simples são as informações de endereço do usuário: um usuário altera um endereço para correspondência na réplica R1 e um administrador altera o mesmo endereço para correspondência na réplica R2. Um valor gravado é propagado até que outro valor seja selecionado sobre esse valor pelo mecanismo de reconciliação de colisão. Desde que um valor continue a "vencer" em relação a outros valores no processo de resolução de colisão, o valor continuará a ser propagado. Por fim, esse valor "vencedor" será propagado para R1, R2 e todas as outras réplicas se nenhuma outra alteração for feita.

A resolução de colisão é um problema para aplicativos que fazem suposições sobre a consistência interna de objetos ou conjuntos de objetos. Por exemplo, um serviço de gerenciamento de alocação de largura de banda de rede armazena dados de largura de banda de rede para um determinado segmento de rede no diretório em um objeto O1. O objeto contém a largura de banda disponível em bits por segundo e a largura de banda máxima que qualquer usuário pode reservar. O serviço espera que a largura de banda reservável do usuário seja sempre menor ou igual à largura de banda disponível.

Considere a seguinte sequência de eventos:

-   O objeto no estado inicial totalmente replicado fornece a largura de banda disponível como 56 kilobits por segundo e a largura de banda reservável do usuário como 9.600 bits por segundo.
-   Um administrador na réplica R ₁ altera os valores para 64K e 19.200, respectivamente.
-   Um administrador na réplica R ₂ altera os valores para 10 milhões e 1 milhão, respectivamente, antes que a atualização do R ₁ chegue.

Supondo que os atributos em questão tenham números de versão iguais quando ocorrerem as atualizações, há uma pequena, mas real possibilidade de que o objeto acabe com uma largura de banda máxima de 64K e um máximo reservável de usuário de 1 milhão — se o aplicativo executar as atualizações como operações de gravação separadas. O aplicativo sempre deve atualizar ambas as propriedades em uma única operação.

 

 