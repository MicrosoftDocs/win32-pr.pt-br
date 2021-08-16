---
title: Impacto sobre Directory-Enabled aplicativos
description: Este tópico descreve o impacto em aplicativos habilitados para diretório quando ocorrem distorções de versão, atualizações parciais ou colisões.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601a5bbffda08f0789875176193977cbecfc34596a9900c870f81cfd677b9ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187671"
---
# <a name="impact-on-directory-enabled-applications"></a>Impacto sobre Directory-Enabled aplicativos

## <a name="version-skew"></a>Distorção de versão

A distorção de versão ocorre quando os aplicativos leem os mesmos objetos de réplicas diferentes antes que uma alteração seja replicada. Os aplicativos que lêem a réplica remota reconhecem o objeto inalterado. A distorção de versão é um problema quando um determinado aplicativo ou conjunto de aplicativos usa os dados no diretório para interoperar.

Por exemplo, um Serviço RPC pode publicar seus pontos de extremidade no diretório usando APIs RPC padrão (como [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta)). Os clientes se conectam ao serviço procurando o ponto de extremidade desejado no diretório ( [**RpcNsBindingLookupBegin,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)e assim por diante) e associação a ele.

Suponha que um Serviço RPC S publique o ponto de extremidade Es e, posteriormente, se mova para um computador diferente. O ponto de extremidade original Es é alterado para E<sub>s2,</sub> refletindo o endereço do novo computador. Os clientes que lêem réplicas remotas do serviço de diretório não podem se conectar ao serviço até que o ponto de extremidade atualizado seja replicado. No entanto, mover um serviço de um computador para outro é uma ocorrência rara; portanto, essa interrupção/atraso raramente deve ser encontrada, especialmente se a movimentação do serviço for bem planejada.

## <a name="partial-updates"></a>Atualizações parciais

Em geral, a atualização parcial ocorre quando um aplicativo está lendo um conjunto de dados enquanto outro aplicativo está escrevendo no mesmo conjunto de dados. Essa é uma situação que pode ocorrer com qualquer aplicativo em um sistema com vários domínios. Há muitas maneiras de isso ocorrer. Você pode ter mais de um aplicativo escrevendo no mesmo conjunto de dados ao mesmo tempo. Se você olhar dessa forma, o serviço de replicação de diretório será apenas outro aplicativo que pode estar escrevendo no mesmo conjunto de dados que outro aplicativo pode estar lendo. Isso pode ser um possível problema para um aplicativo. No entanto, a janela de tempo em que uma atualização parcial pode afetar seu aplicativo é relativamente pequena. Isso raramente deve ser um problema para aplicativos que não dependem da sincronização de vários objetos. Se seu aplicativo for altamente dependente da sincronização de um conjunto relacionado de objetos, considere os efeitos de uma atualização parcial no design do aplicativo.

Em termos de replicação de diretório, a atualização parcial ocorre quando os aplicativos leem o mesmo conjunto de objetos de réplicas diferentes enquanto a replicação está em andamento. Os aplicativos na réplica remota veem algumas, mas não todas, das alterações.

> [!Note]  
> A janela na qual a atualização parcial pode afetar um aplicativo é pequena: o aplicativo deve começar a ler objetos enquanto a replicação de entrada está em andamento, depois que um ou mais dos objetos alterados relacionados foram recebidos, mas antes que todos tenham sido recebidos. O tempo entre as atualizações na réplica de origem afeta diretamente o tamanho dessa janela– as atualizações que ocorrem próximas no tempo são replicadas próximas no tempo. A atualização parcial pode ser um problema quando um aplicativo usa um conjunto relacionado de objetos.

 

Por exemplo, um serviço de acesso remoto pode usar o diretório para armazenar dados de política e perfil. Os dados da política são armazenados em um conjunto de objetos e o perfil em outro conjunto. Quando um usuário se conecta ao serviço de acesso remoto, o serviço de acesso remoto lê a política para determinar se o usuário tem permissão para se conectar e, se for o caso, qual perfil aplicar à sessão do usuário. A atualização parcial pode afetar o serviço de acesso remoto de várias maneiras:

-   Se a política for complexa e consistir em vários objetos, o serviço de acesso remoto poderá ler uma política parcialmente atualizada, resultando em negação incorreta ou concessão de serviço ao usuário, incapacidade de processar a política devido a inconsistências internas e assim por diante.
-   Se a política e os perfis foram atualizados, o serviço pode processar corretamente a política, mas aplicar um perfil desleais, pois os objetos de política foram replicados, mas os objetos de perfil não foram.
-   Se o perfil for complexo e consistir em vários objetos, o serviço poderá processar corretamente a política, mas aplicar um perfil parcialmente atualizado porque os objetos de política foram replicados, mas apenas alguns dos objetos de perfil fizeram isso.

## <a name="collisions"></a>Colisões

As colisões ocorrem quando os mesmos atributos de duas ou mais réplicas de um determinado objeto são alterados durante o mesmo intervalo de replicação. O processo de replicação reconcilia a colisão; devido à reconciliação, um usuário ou aplicativo pode "ver" um valor diferente do que escreveu.

Um exemplo simples são informações de endereço de usuário: um usuário altera um endereço de email na réplica R1 e um administrador altera o mesmo endereço de email na réplica R2. Um valor gravado se propaga até que outro valor seja selecionado sobre esse valor pelo mecanismo de reconciliação de colisão. Desde que um valor continue a "ganhar" em relação a outros valores no processo de resolução de colisão, o valor continuará sendo propagado. Por fim, esse valor "vencedor" será propagado para R1,R2 e todas as outras réplicas se nenhuma outra alteração for feita.

A resolução de colisão é um problema para aplicativos que fazem suposições sobre a consistência interna de objetos ou conjuntos de objetos. Por exemplo, um serviço de gerenciamento de alocação de largura de banda de rede armazena dados de largura de banda de rede para um determinado segmento de rede no diretório em um objeto O1. O objeto contém a largura de banda disponível em bits por segundo e a largura de banda máxima que qualquer usuário pode reservar. O serviço espera que a largura de banda reserval do usuário sempre seja menor ou igual à largura de banda disponível.

Considere a seguinte sequência de eventos:

-   O objeto no estado totalmente replicado inicial fornece a largura de banda disponível como 56 quilobits por segundo e a largura de banda reserval do usuário como 9.600 bits por segundo.
-   Um administrador na réplica R altera os valores para 64k e 19.200, respectivamente.
-   Um administrador na réplica R altera os valores para 10 milhões e 1 milhão, respectivamente, antes da atualização do R chegar.

Supondo que os atributos em questão tenham números de versão iguais quando as atualizações ocorrem, há uma possibilidade pequena, mas real, de que o objeto acabará com uma largura de banda máxima de 64k e um máximo de reserva de usuário de 1 milhão— se o aplicativo executar as atualizações como operações de gravação separadas. O aplicativo sempre deve atualizar as duas propriedades em uma única operação.

 

 