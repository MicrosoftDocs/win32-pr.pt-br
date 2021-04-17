---
description: Um provedor de cópia de sombra deve estar em conformidade com as diretrizes para garantir a compatibilidade do solicitante.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportamentos necessários para provedores de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f451dea7154a313cd64a3a46fbcc3b5fe663ec12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763962"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportamentos necessários para provedores de cópia de sombra

Um provedor de cópia de sombra deve estar em conformidade com as diretrizes para garantir a compatibilidade do solicitante. Em tempo de execução, um aplicativo de backup ou qualquer outro solicitante que use cópias de sombra deve funcionar corretamente sem qualquer conhecimento de detalhes específicos de implementação do provedor.

## <a name="automagic-resource-management"></a>Gerenciamento de recursos automagic

Deve ser possível que o solicitante simplesmente adicione um volume a um conjunto de cópias de sombra. O solicitante pode especificar atributos de cópia de sombra, como o **VSS \_ VolSnap \_ attr \_ transportável**, **VSS \_ VolSnap \_ attr \_ diferencial** e/ou o **Plex de atributo de VolSnap do VSS \_ \_ \_** no [**\_ \_ \_ contexto de instantâneo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context). O provedor deve respeitar esses atributos. Se ele não puder honrar esses atributos, ele deverá indicar que o conjunto de cópias de sombra não tem suporte definindo \* *PbIsSupported* em [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) como **false**.

O provedor nunca deve concordar em dar suporte a uma cópia de sombra que não pode ser criada. Se o solicitante não especificar um atributo de plex ou diferencial, o provedor deverá incluir a lógica de automagic para alocar o espaço do subsistema para a cópia de sombra e criar a cópia de sombra usando o método mais apropriado. O provedor de hardware não deve incluir uma API específica do provedor para gerenciar as propriedades de cópia de sombra necessárias.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Os volumes de cópia de sombra criados são Read-Only e ocultos

O VSS define os sinalizadores em cada LUN afetado, de modo que os volumes de cópia de sombra resultantes serão ocultos e somente leitura quando detectados por um computador que executa o Windows Server 2003. Letras de unidade e pastas montadas não são atribuídas automaticamente. O VSS mantém esses sinalizadores durante todo o ciclo de vida de uma cópia de sombra.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>LUNs de cópia de sombra de hardware devem ser de leitura/gravação

O VSS dá suporte a cópias de sombra de hardware somente quando o LUN subjacente é mapeado como leitura/gravação. Isso deve ser feito antes que a cópia de sombra seja criada; Isso não pode ser feito após o fato. Os provedores de hardware não devem modificar esses sinalizadores. Para obter mais informações sobre como o VSS usa esses sinalizadores, consulte [o processo de criação de cópia de sombra](the-shadow-copy-creation-process.md).

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>Não há suporte para a importação automática de cópias de sombra de hardware no serviço de cluster do Windows

O Windows Serviço de cluster não pode acomodar LUNs com assinaturas duplicadas e layout de partição. Os LUNs de cópia de sombra devem ser transportados para um host fora do cluster. Para obter mais informações, consulte [recuperação rápida usando volumes copiados de sombra transportável](fast-recovery-using-transportable-shadow-copied-volumes.md).

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>As cópias de sombra que contêm discos dinâmicos devem ser transportadas para um host diferente

**Antes do Windows Server 2008:** O suporte nativo para discos dinâmicos não pode acomodar LUNs com assinaturas duplicadas e conteúdo de banco de dados de configuração. Os LUNs de cópia de sombra devem ser transportados para um host diferente. O VSS impõe isso por não permitir cópias de sombra de discos dinâmicos de importação automática. Um solicitante não deve importar uma cópia de sombra transportável de volta para o mesmo host.

**A partir do Windows Server 2008:** Essa limitação é removida.

## <a name="providers-are-out-of-process"></a>Os provedores estão fora do processo

Todos os provedores devem ser implementados como componentes COM fora do processo.

## <a name="time-critical-operations"></a>Operações de Time-Critical

Operações longas, como a sincronização de plexes, devem ser iniciadas em [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot). Essa função deve iniciar o trabalho de preparação assíncrona e retornar rapidamente. [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) serve como uma função de "reunião" — o provedor pode esperar de forma síncrona nesse método para a conclusão do trabalho de preparação que foi iniciado pelo **BeginPrepareSnapshot**.

Os provedores não devem adicionar atrasos em [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)ou [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) , pois os aplicativos são congelado durante essas chamadas. **CommitSnapshots** deve retornar em segundos, porque isso é chamado durante a janela de liberação e espera, e o suporte ao kernel do VSS cancelará a liberação e a espera se a versão não for recebida em 10 segundos, o que faria com que o VSS falhasse no processo de criação da cópia de sombra. Se o provedor levar mais de alguns segundos para concluir essa chamada, haverá uma alta probabilidade de que a criação da cópia de sombra falhe.

## <a name="careful-io-during-commitsnapshots"></a>E/s cuidadosa durante CommitSnapshots

Os provedores de hardware não devem precisar fazer nenhuma e/s para os volumes envolvidos na cópia de sombra durante o [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots). Se qualquer e/s for necessária, os provedores não deverão iniciar nenhuma e/s para um volume original ao manipular o método **CommitSnapshots** .

Durante a [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), os drivers de suporte do kernel do VSS bloqueiam a e/s para os volumes originais que estão sendo copiados em sombra. Se o provedor usar e/s síncrona para um volume que está no conjunto de cópias de sombra, essa e/s será bloqueada e o processo de confirmação da cópia de sombra será travado. O provedor não deve chamar nenhuma API do Win32 durante o **CommitSnapshots** , pois terá uma alta probabilidade de causar e/s e um deadlock. O tempo limite de suporte do kernel do VSS interromperá esse deadlock após 10 segundos, mas isso fará com que a criação da cópia de sombra falhe.

Se a e/s precisar ser tentada, ela deve ser executada de forma assíncrona. A e/s não será concluída até que todos os provedores tenham retornado dos seus métodos [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Em geral, é melhor executar essas operações na chamada [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) .

## <a name="readwrite-shadow-copy-luns"></a>Leitura/gravação de LUNs de cópia de sombra

Nesta versão, o VSS dá suporte apenas a LUNs de cópia de sombra de leitura/gravação, mesmo que os volumes sejam expostos como somente leitura. O motivo é que o sistema precisa alterar estruturas de dados em disco, como:

-   Assinatura de disco, que muda durante o processo de cópia de sombra
-   Estruturas de dados relacionadas à partição, incluindo aquelas indicando que a partição é somente leitura, oculta, uma cópia de sombra e não deve ser atribuída a uma letra de unidade.

## <a name="unique-page-83-information"></a>Informações da página exclusiva 83

O LUN original e o LUN de cópia de sombra criado recentemente devem ter pelo menos um identificador de armazenamento exclusivo na página dados do 83. Pelo menos um identificador de armazenamento \_ com um tipo de 1, 2, 3 ou 8 e uma associação de 0 deve ser exclusivo no LUN original e no LUN de cópia de sombra criado recentemente.

 

 



