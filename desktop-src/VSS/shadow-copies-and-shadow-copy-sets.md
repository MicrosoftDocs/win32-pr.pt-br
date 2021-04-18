---
description: Uma cópia de sombra é um instantâneo de um volume que duplica todos os dados que são mantidos nesse volume, em um instante bem definido. O VSS identifica cada cópia de sombra por um GUID persistente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Cópias de sombra e conjuntos de cópias de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811383"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Cópias de sombra e conjuntos de cópias de sombra

Uma [*cópia de sombra*](vssgloss-s.md) é um instantâneo de um volume que duplica todos os dados que são mantidos nesse volume, em um instante bem definido. O VSS identifica cada cópia de sombra por um GUID persistente.

Um [*conjunto de cópias de sombra*](vssgloss-s.md) é uma coleção de cópias de sombra de vários volumes obtidos ao mesmo tempo. O VSS identifica cada conjunto de cópias de sombra por um GUID persistente.

A forma como um fornecedor específico de hardware ou software opta por implementar cópias de sombra é completamente a seu critério. Depois que uma cópia de sombra é criada, há efetivamente duas imagens do volume copiado por sombra disponíveis para o sistema: o volume original, que pode ser acessado de forma convencional; e os dados copiados, que podem ser acessados por meio da API do VSS.

Isso permite que dois conjuntos de atividades ocorram ao mesmo tempo:

-   Aplicativos comuns no sistema podem continuar ou retomar rapidamente usando o volume original, atualizando os dados no disco.
-   Os aplicativos que estão usando a API do solicitante do VSS para acessar o volume copiado por sombra podem executar backups ou operações semelhantes.

As cópias de sombra não precisam ser implementadas da mesma maneira para cada arquivo, diretório ou volume. Implementações diferentes do mecanismo de cópia de sombra ([*provedores*](vssgloss-p.md)) podem usar abordagens diferentes para criar uma cópia de sombra. No entanto, para todos os aplicativos que estão usando a API do VSS, todas as cópias de sombra devem ser iguais.

Para obter informações sobre a implementação padrão do provedor do Windows, consulte [provedor do sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Estado de cópia de sombra padrão

Embora o sistema de arquivos libere todos os buffers de e/s antes de criar uma cópia de sombra, isso não garantirá que a e/s incompleta seja manipulada corretamente.

Portanto, supondo que o sistema não tenha aplicativos habilitados para VSS, os dados em uma cópia de sombra são considerados em um [*estado consistente de falha*](vssgloss-c.md). Uma cópia de sombra em um estado consistente com falhas contém uma imagem do disco que é a mesma que a que existe após um desligamento catastrófico do sistema. Todos os arquivos que estavam abertos ainda existirão no volume, mas não há garantia de que estejam livres de operações de e/s incompletas ou dados corrompidos.

Embora o estado de falha consistente não lide totalmente com todos os problemas associados à definição de um conjunto de backup estável (consulte [problemas comuns de backup de volume](common-volume-backup-issues.md)), ele tem várias vantagens em relação ao conjunto de backup que as operações de backup convencionais teriam para usar:

-   Um volume contido em uma cópia de sombra, mesmo em um estado consistente em caso de falhas, ainda contém todos os arquivos. Um conjunto de backup criado sem uma cópia de sombra não conteria todos os arquivos abertos no momento do backup. Os arquivos mantidos abertos no momento da operação de backup são excluídos do backup.
-   A cópia de sombra do volume é criada em um instante no tempo e não atravessando um sistema de arquivos ativo, que normalmente requer muito mais tempo.

Os aplicativos em um sistema que não reconhecem o VSS — processadores de texto, editores e assim por diante — provavelmente terão seus arquivos deixados em um estado consistente com falhas. No entanto, os aplicativos com reconhecimento de VSS (gravadores) podem coordenar suas ações para que o estado de seus arquivos na cópia de sombra seja bem definido e consistente.

## <a name="shadow-copy-freeze-and-thaw"></a>Congelar e descongelar cópias de sombra

A criação de cada operação de cópia de sombra do VSS tem como colchete [*congelar*](vssgloss-f.md) e [*descongelar*](vssgloss-t.md) eventos, que os gravadores usam para colocar seus arquivos em um estado estável antes da cópia de sombra.

Ter congelar e descongelar eventos como parte do modelo VSS significa:

-   Manipular o evento Freeze significa que aqueles que estão desenvolvendo gravadores devem ter um ponto claramente delimitado no ciclo de backup, no qual eles garantem que todas as operações de gravação no disco sejam interrompidas e que os arquivos estejam em um estado bem definido para backup.
-   Manipular o evento descongelar fornece o mecanismo para que os gravadores retomem gravações no disco e limpem quaisquer arquivos temporários ou outras informações de estado temporários que foram criadas em associação com a cópia de sombra.
-   A janela padrão entre os eventos Freeze e descongelar é curta (geralmente 60 segundos); Portanto, a interrupção real de qualquer serviço que um gravador fornece pode ser minimizada.
-   O tratamento de outros eventos (como PrepareForSnapshot) que antecedem e seguir os eventos Freeze e descongelar, respectivamente, fornece a flexibilidade necessária para permitir que os gravadores concluam operações complicadas para dar suporte a cópias de sombra.

 

 



