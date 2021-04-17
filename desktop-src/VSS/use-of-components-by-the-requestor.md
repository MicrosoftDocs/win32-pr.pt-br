---
description: Além de executar um backup ou restauração e supervisionar cópias de sombra, um solicitante deve gerenciar informações sobre os componentes dos gravadores com os quais interage.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Uso de componentes pelo solicitante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83efdb9e80ac0331289c3b611978e66a58098de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501740"
---
# <a name="use-of-components-by-the-requester"></a>Uso de componentes pelo solicitante

Além de executar um backup ou restauração e supervisionar cópias de sombra, um solicitante deve gerenciar informações sobre os componentes dos gravadores com os quais interage. A seleção de componentes e o caminho lógico são usados para incluir ou excluir dados de um backup e para decidir quais informações de componente estão incluídas no documento de componentes de backup.

## <a name="requester-component-selection-during-backup"></a>Seleção de componente do solicitante durante o backup

Durante as operações de backup, um solicitante importa dados do componente de metadados do gravador usando os métodos [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (consulte [visão geral da inicialização do backup](overview-of-backup-initialization.md) para obter mais informações).

Depois de examinar as informações do gravador com a interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , um solicitante decide quais gravadores ele fará o backup e, em uma extensão limitada, qual dos componentes de um determinado gravador ele fará o backup.

Ao fazer backup de um gravador, um solicitante:

-   Deve [*incluir explicitamente*](vssgloss-e.md) todos os não selecionáveis do gravador para componentes de backup sem selecionável para os ancestrais de backup usando [**IVssBackupComponents:: addcomponente**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para adicionar o componente ao documento de componentes de backup
-   Pode incluir explicitamente qualquer uma das selecionáveis do gravador para componentes de backup usando [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para adicionar o componente ao documento de componentes de backup
-   Se um componente selecionável para backup definir um [*conjunto de componentes*](vssgloss-c.md), sua inclusão explícita [*incluirá implicitamente*](vssgloss-i.md) todos os membros do conjunto de componentes — seja selecionável para backup ou não. Esses componentes não são adicionados ao documento de componentes de backup.

Ao adicionar um selecionável para o componente de backup ou um não selecionável para componentes de backup sem selecionável para os ancestrais de backup para seu documento de componentes de backup, um solicitante especifica o seguinte:

-   A instância do gravador que gerencia o componente
-   O identificador de classe do gravador
-   O [*caminho lógico*](vssgloss-l.md) do componente (que pode ser **nulo**)
-   O nome do componente

Se um componente não corresponder à especificação, um erro será retornado.

Se esse componente existir, o VSS criará uma interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) para o componente no documento de componentes de backup. Essas informações estarão acessíveis e modificáveis pelo gravador e pelo solicitante. Para um componente selecionável que define um [*conjunto de componentes*](vssgloss-c.md), ele descreve não apenas as propriedades do componente, mas também todos os subcomponentes que ele contém.

As informações sobre componentes adicionados implicitamente não estão disponíveis no documento componentes de backup. Além disso, nenhuma informação de arquivo está disponível no documento componentes de backup. Para obter essas informações, o solicitante precisará examinar os documentos de metadados do gravador (que já terão sido lidos) no contexto dos componentes armazenados selecionados no documento componentes de backup.

## <a name="requester-component-selection-during-restore"></a>Seleção de componente do solicitante durante a restauração

Durante as operações de restauração, um solicitante não deve importar informações de componentes dos gravadores atualmente ativos no sistema por meio de [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), porque o estado dos processos atualmente em execução não refletirá necessariamente o estado dos processos quando um backup foi feito.

Ele ainda deve gerar um [*evento de identificação*](vssgloss-i.md) via [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), tanto para criar um *evento de identificação* quanto para determinar quais gravadores estão atualmente no sistema e seu status.

O solicitante recupera o documento de componentes de backup armazenados durante sua inicialização, bem como documentos de metadados do gravador armazenados (consulte [visão geral da inicialização da restauração](overview-of-restore-initialization.md) para obter mais informações).

A inclusão de componentes durante o backup é basicamente a mesma para a restauração, exceto que você deve considerar [*selecionável para restauração*](vssgloss-s.md) junto com o [*caminho lógico*](vssgloss-l.md)— não [*selecionável para backup*](vssgloss-s.md).

No entanto, há algumas diferenças:

-   Se um componente já tiver sido [*incluído explicitamente*](vssgloss-e.md) no documento de componentes de backup durante o backup, se ele estiver incluído para restauração (explícita ou implicitamente), [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) será usado para adicioná-lo explicitamente ao documento de componentes de backup para restauração.
-   Se um componente foi [*implicitamente incluído*](vssgloss-i.md) no backup e não é selecionável para restauração sem selecionável para Restore ancestrais — que, no caso de backup, significaria a necessidade de inclusão explícita — o componente não é incluído explicitamente (ou seja, não é adicionado ao documento de componentes de backup usando [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)). Esse componente deve ser considerado implicitamente selecionado para restauração.
-   Desses componentes selecionados implicitamente para backup (independentemente de o componente ter sido selecionável para backup ou não), somente aqueles que são selecionáveis para restauração podem ser adicionados ao documento de componentes de backup usando [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Selecionável para os componentes de restauração pode definir um [*conjunto de componentes*](vssgloss-c.md) para restauração — da mesma forma que selecionável para componentes de backup. Essa selecionável para o componente de restauração define esse conjunto de componentes para a operação de restauração.

Um gravador sem componentes selecionados explicitamente para restauração antes da geração de um evento de [*Prerestore*](vssgloss-p.md) não receberá eventos VSS.

Os solicitantes e gravadores podem acessar informações de componentes armazenados usando a interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Por meio da interface **IVssComponent** , os gravadores podem modificar algumas das configurações dos componentes incluídos explicitamente no documento componentes de backup para dar suporte a uma restauração (como o [*destino de restauração*](vssgloss-r.md)). Se ele definir um conjunto de componentes, as modificações do gravador de um componente explicitamente incluído serão propagadas para seus [*Subcomponentes*](vssgloss-s.md). Além disso, a interface fornece um mecanismo para passar informações sobre o êxito da restauração e a falha entre o gravador e o solicitante.

Como durante o backup, não há informações suficientes no próprio documento de componentes de backup para implementar a restauração. Novamente, os documentos de metadados do gravador serão solicitados a fornecer informações sobre os caminhos reais dos arquivos a serem restaurados e descobrir quais componentes não selecionáveis fazem parte do conjunto de componentes do componente selecionável e, portanto, precisam ser restaurados.

Consulte [trabalhando com a seleção e caminhos lógicos](working-with-selectability-and-logical-paths.md) para obter informações sobre os tipos de seleção e seu uso.

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Uso de informações de documento de componente do gravador pelo solicitante

Cada componente é identificado exclusivamente pela ID de [*classe do gravador*](vssgloss-w.md) de seu gravador pai, seu nome e seu [*caminho lógico*](vssgloss-l.md).

O solicitante pode usar a interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) retornada pelo método [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) para obter informações sobre cada componente armazenado.

O nome do componente e o caminho lógico (entre outros itens) podem ser encontrados por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) retornada por [**IVssWriterComponentsExt:: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Durante a fase de restauração, o solicitante deve chamar [**IVssWriterComponentsExt:: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) ou [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) somente após a chamada para [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) foi retornada, para dar tempo para o gravador atualizar o documento de componentes de backup. Um exemplo de tal atualização seria alterar o destino de restauração.

 

As informações sobre cada gravador pai do componente selecionável armazenado podem ser encontradas usando [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Com essas informações, os documentos de metadados do gravador podem ser consultados e o documento correspondente identificado. Em seguida, usando o [*caminho lógico*](vssgloss-l.md), o solicitante pode identificar os componentes não selecionáveis dependentes para cada componente selecionável, ou seja, identificar todos os membros do [*conjunto de componentes*](vssgloss-c.md)do componente selecionável.

Usando a interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , o solicitante agora tem informações completas sobre o componente, incluindo a especificação de caminho (da interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) ) — para componentes selecionáveis e não selecionáveis, ele precisa fazer backup ou restaurar.

Esse é um dos motivos pelos quais é vital que um solicitante salve o estado de seus próprios documentos de componentes de backup e os documentos de metadados do gravador dos gravadores em que está fazendo backup.

Consulte [trabalhando com a seleção e caminhos lógicos](working-with-selectability-and-logical-paths.md) para obter informações mais detalhadas.

 

 
