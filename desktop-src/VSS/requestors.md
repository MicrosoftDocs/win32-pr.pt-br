---
description: Um solicitante é qualquer aplicativo que use a API do VSS (especificamente a interface IVssBackupComponents) para solicitar os serviços do Serviço de Cópias de Sombra de Volume para criar e gerenciar cópias de sombra e conjuntos de cópias de sombra de um ou mais volumes.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e7fa7b1718b0da278dabb164fbffee43c939cd688c150e202bfafc4731a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866376"
---
# <a name="requesters"></a>Solicitantes

Um [*solicitante*](vssgloss-r.md) é qualquer aplicativo que use a API do VSS (especificamente a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ) para solicitar os serviços do serviço de cópias de sombra de volume para criar e gerenciar cópias de sombra e conjuntos de cópias de sombra de um ou mais volumes.

O exemplo mais comum de um solicitante (e o único abordado nesta documentação) é um aplicativo de backup/restauração com reconhecimento de VSS, que usa dados copiados por sombra como uma fonte estável para suas operações de backup.

Além de iniciar cópias de sombra, os aplicativos de solicitação de backup/recuperação se comunicam com produtores de dados (gravadores) para coletar informações sobre o sistema e para sinalizar gravadores para preparar seus dados para backup.

## <a name="requester-state"></a>Estado do solicitante

Um solicitante mantém suas informações de estado em um objeto de metadados baseado em XML chamado documento de componentes de backup. Os metadados do solicitante são necessários, mas não é suficiente para permitir que um solicitante faça backup e, em seguida, restaure um sistema de arquivos. Os motivos para isso são os seguintes:

-   Durante uma operação de backup, apenas um subconjunto de todos os componentes envolvidos no backup — não [*selecionável para*](vssgloss-s.md) componentes de backup sem selecionáveis para os ancestrais de backup e selecionáveis para os componentes de backup que foram [*incluídos explicitamente*](vssgloss-e.md) no backup — tiveram suas informações adicionadas ao documento de componentes de backup do solicitante.
-   As informações até mesmo para os componentes adicionados ao documento de componentes de backup estão incompletas: as especificações de arquivo e caminho não estão incluídas.
-   Durante as operações de restauração, um componente [*incluído implicitamente*](vssgloss-i.md) no backup pode ser [*selecionável para restauração*](vssgloss-s.md) e, portanto, pode ser incluído explicitamente na restauração. Isso exigirá a atualização do documento de componentes de backup do solicitante com informações de cópias armazenadas do documento de metadados do gravador de um gravador.

Para permitir a especificação completa de uma operação de backup ou restauração, a API do VSS permite que o solicitante consulte os metadados da execução dos gravadores (durante os backups) ou examine os metadados do gravador armazenado (durante as restaurações). Além disso, um gravador pode modificar as informações do componente no documento de componentes de backup no decorrer de uma operação de backup ou restauração.

Usando as informações sobre quais componentes foram selecionados para backup e restauração e as regras sobre a seleção de componentes (para obter mais informações, consulte [Configurando a organização do componente](definition-of-components-by-writers.md) e [trabalhando com a escolha e os caminhos lógicos](working-with-selectability-and-logical-paths.md)), um solicitante pode determinar quais arquivos de qual gravador precisa fazer backup ou restaurar e onde ele pode encontrar esses arquivos.

Como parte de um backup, os metadados do solicitante e do gravador devem ser armazenados para que possam ser usados na restauração. Por outro lado, as operações de restauração exigem a recuperação dos documentos de metadados do gravador e dos componentes de backup antigos para obter instruções completas sobre a restauração de arquivos.

## <a name="requester-interprocess-communication"></a>Comunicação entre processos do solicitante

O solicitante mantém o controle sobre as operações de backup e restauração do VSS, gerando eventos COM por meio de várias chamadas na API do solicitante. Essas chamadas podem fazer o seguinte:

-   Faça solicitações dos provedores, por exemplo, [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) faz com que o provedor crie uma cópia de sombra do volume selecionado.
-   Disparar os gravadores para retornar informações, por exemplo, [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) permite que o solicitante obtenha o documento de metadados do gravador de cada gravador.
-   Exigir que os gravadores se preparem ou manipulem várias fases das operações de cópia de sombra e backup, por exemplo, [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) Signal Writers para configurar o congelamento de e/s.

Um solicitante recebe informações dos gravadores por meio de documentos de metadados do gravador em tempo real ou armazenados e com o uso da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , que o gravador pode atualizar.

## <a name="life-cycle-of-a-requester-during-backup"></a>Ciclo de vida de um solicitante durante o backup

Veja a seguir um resumo do ciclo de vida do solicitante para backup:

1.  Instanciar e inicializar interfaces de API do VSS.
2.  Contate os gravadores e recupere suas informações.
3.  Escolha os dados para fazer backup.
4.  Solicite uma cópia de sombra do provedor.
5.  Faça backup dos dados.
6.  Libere a interface e a cópia de sombra.

## <a name="life-cycle-of-a-requester-during-restore"></a>Ciclo de vida de um solicitante durante a restauração

O ciclo de vida da restauração não requer uma cópia de sombra, mas ainda requer a cooperação do gravador:

1.  Instanciar interfaces de API do VSS.
2.  Inicialize o solicitante para a operação de restauração carregando um documento de componentes de backup armazenados.
3.  Recuperar documentos de metadados do gravador armazenado e componentes de backup.
4.  Entre em contato com os gravadores para inicializar a cooperação.
5.  Verifique se há atualizações do gravador no documento de componentes de backup.
6.  Restaurar os dados.

 

 



