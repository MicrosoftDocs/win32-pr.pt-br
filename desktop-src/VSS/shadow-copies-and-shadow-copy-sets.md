---
description: Uma cópia de sombra é um instantâneo de um volume que duplica todos os dados mantidos nesse volume em um instante bem definido no tempo. O VSS identifica cada cópia de sombra por um GUID persistente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Cópias de sombra e conjuntos de cópias de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764478c371cf4a622612865ef7a529955780d82847125874253533d331c195f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998146"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Cópias de sombra e conjuntos de cópias de sombra

Uma [*cópia de sombra*](vssgloss-s.md) é um instantâneo de um volume que duplica todos os dados mantidos nesse volume em um instante bem definido no tempo. O VSS identifica cada cópia de sombra por um GUID persistente.

Um [*conjunto de cópias de*](vssgloss-s.md) sombra é uma coleção de cópias de sombra de vários volumes feitos ao mesmo tempo. O VSS identifica cada conjunto de cópias de sombra por um GUID persistente.

Como um fornecedor de hardware ou software específico opta por implementar cópias de sombra é completamente a seu critério. Depois que uma cópia de sombra é criada, há efetivamente duas imagens do volume copiado em sombra disponíveis para o sistema: o volume original, que pode ser acessado convencionalmente; e os dados copiados, que podem ser acessados por meio da API do VSS.

Isso permite que dois conjuntos de atividades ocorrem ao mesmo tempo:

-   Aplicativos comuns no sistema podem continuar ou retomar rapidamente usando o volume original, atualizando dados no disco.
-   Os aplicativos que estão usando a API do solicitante vsS para acessar o volume copiado por sombra podem executar backups ou operações semelhantes.

Cópias de sombra não precisam ser implementadas da mesma maneira para cada arquivo, diretório ou volume. Implementações diferentes do mecanismo de cópia de sombra ( provedores ) podem usar [*abordagens*](vssgloss-p.md)diferentes para criar uma cópia de sombra. No entanto, para todos os aplicativos que estão usando a API do VSS, todas as cópias de sombra devem aparecer da mesma forma.

Para obter informações sobre a implementação Windows provedor padrão, consulte [Provedor de Sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Estado de cópia de sombra padrão

Embora o sistema de arquivos libera todos os buffers de E/S antes de criar uma cópia de sombra, isso não garantirá que a E/S incompleta seja tratada corretamente.

Portanto, supondo que o sistema não tenha aplicativos habilitados para VSS, os dados em uma cópia de sombra devem estar em um estado consistente [*com falhas*](vssgloss-c.md). Uma cópia de sombra em um estado consistente com falhas contém uma imagem do disco que é a mesma que existiria após um desligamento catastrófico do sistema. Todos os arquivos que estavam abertos ainda existirão no volume, mas não há garantia de que eles estarão livres de operações de E/S incompletas ou dados de corrupção.

Embora o estado consistente com falhas não lidar totalmente com todos os problemas associados à definição de um conjunto de backup estável (consulte Problemas comuns de backup de [volume),](common-volume-backup-issues.md)ele tem várias vantagens em relação ao conjunto de backup que as operações de backup convencionais teriam que usar:

-   Um volume contido em uma cópia de sombra, mesmo em um estado consistente com falhas, ainda contém todos os arquivos. Um conjunto de backup criado sem uma cópia de sombra não conteria todos os arquivos abertos no momento do backup. Os arquivos mantidos abertos no momento da operação de backup são excluídos do backup.
-   A cópia de sombra do volume é criada em um instante no tempo e não atravessando um sistema de arquivos ativo, o que normalmente requer muito mais tempo.

Aplicativos em um sistema que não são compatíveis com VSS , processadores de palavras, editores e assim por diante, provavelmente terão seus arquivos deixados em um estado consistente com falhas. No entanto, os aplicativos com conhecimento de VSS (autores) podem coordenar suas ações para que o estado de seus arquivos na cópia de sombra seja bem definido e consistente.

## <a name="shadow-copy-freeze-and-thaw"></a>Congelamento e descongelamento de cópia de sombra

A criação de cada operação de cópia de [](vssgloss-t.md) sombra do VSS é entre colchetes pelos eventos [*Congelar*](vssgloss-f.md) e Descongelar, que os autores usam para colocar seus arquivos em um estado estável antes da cópia de sombra.

Ter eventos de congelamento e descongelamento como parte do modelo VSS significa:

-   Manipular o evento Freeze significa que aqueles que estão desenvolvendo autores devem ter um ponto claramente delineado no ciclo de backup em que garantem que todas as operações de gravação no disco sejam interrompidas e que os arquivos estão em um estado bem definido para backup.
-   Manipular o evento Descongelar fornece o mecanismo para que os autores retomem gravações no disco e limpem quaisquer arquivos temporários ou outras informações de estado temporário que foram criadas em associação com a cópia de sombra.
-   A janela padrão entre os eventos Congelamento e Descongelamento é curta (normalmente 60 segundos); portanto, a interrupção real de qualquer serviço que um autor fornece pode ser minimizada.
-   A manipulação de outros eventos (como PrepareForSnapshot) anteriores e após os eventos Congelamento e Descongelamento, respectivamente, fornece a flexibilidade necessária para permitir que os autores concluam operações complicadas para dar suporte a cópias de sombra.

 

 



