---
description: O VSS foi projetado para resolver os problemas descritos em problemas comuns de backup de volume.
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: O modelo VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781303"
---
# <a name="the-vss-model"></a>O modelo VSS

O VSS foi projetado para resolver os problemas descritos em [problemas comuns de backup de volume](common-volume-backup-issues.md).

O modelo VSS inclui o seguinte:

-   O mecanismo de cópia de sombra. O VSS fornece captura rápida de volume do estado de um disco em um instante no tempo — uma [*cópia de sombra*](vssgloss-s.md) do volume. Essa cópia de volume existe lado a lado com o volume ativo e contém cópias de todos os arquivos em disco efetivamente salvas e disponíveis como um dispositivo separado.
-   Estado de arquivo consistente por meio da coordenação de aplicativos. O VSS fornece um mecanismo de comunicação interprocessamento baseado em eventos com base em um evento que os processos participantes podem usar para determinar o estado do sistema em relação a operações de backup, restauração e cópia de sombra (captura de volume). Esses eventos definem os estágios pelos quais os aplicativos que modificam os dados no disco ([*gravadores*](vssgloss-w.md)) podem colocar todos os seus arquivos em um estado consistente antes da criação da cópia de sombra.
-   Minimizando o tempo de inatividade do aplicativo. A cópia de sombra do VSS existe em paralelo com uma cópia dinâmica do volume do qual será feito backup, portanto, exceto pelo breve período da preparação e da criação da cópia de sombra, um aplicativo pode continuar seu trabalho. O tempo necessário para realmente criar uma cópia de sombra, que ocorre entre [*congelar*](vssgloss-f.md) e [*descongelar*](vssgloss-t.md) eventos, normalmente leva cerca de um minuto.

    Enquanto a preparação de um gravador para uma cópia de sombra, incluindo a liberação de e/s e O estado de salvamento (consulte [visão geral das tarefas de pré-backup](overview-of-pre-backup-tasks.md)), pode não ser trivial, ela é significativamente menor do que o tempo necessário para realmente fazer backup de um volume — que para grandes volumes pode levar horas.

-   Interface unificada para VSS. O VSS abstrai os mecanismos de cópia de sombra em uma interface comum ao mesmo tempo em que permite que um fornecedor de hardware adicione e gerencie os recursos exclusivos de seus próprios provedores. Qualquer aplicativo de backup ([*solicitante*](vssgloss-r.md)) e qualquer gravador deve ser capaz de ser executado em qualquer sistema de armazenamento em disco que dê suporte à interface VSS.
-   Backup de multivolume. O VSS dá suporte a [*conjuntos de cópias de sombra*](vssgloss-s.md), que são coleções de cópias de sombra, em vários tipos de volumes de disco de vários fornecedores. Todas as cópias de sombra em um conjunto de cópias de sombra serão criadas com o mesmo carimbo de data/hora e apresentarão o mesmo estado de disco para um estado de disco de multivolume.
-   Suporte à cópia de sombra nativa. A partir do Windows XP, o suporte à cópia de sombra está disponível por meio do VSS como parte nativa do sistema operacional Windows. Desde que pelo menos um disco NTFS esteja presente em um sistema, esses sistemas podem ser configurados para dar suporte a cópias de sombra de todos os sistemas de disco montados neles.

 

 



