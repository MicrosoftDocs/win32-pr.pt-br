---
description: A seleção de restauração permite que o solicitante determine quando um componente pode ser restaurado individualmente.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Trabalhando com a seleção para restauração e subcomponentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d988f4c4e029c7dd8623ad22fcaee7662d33e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501725"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Trabalhando com a seleção para restauração e subcomponentes

A seleção de restauração permite que o solicitante determine quando um componente pode ser restaurado individualmente. Um componente que foi incluído para backup pode aparecer de uma das duas maneiras:

-   Um componente pode ter sido [*incluído explicitamente*](vssgloss-e.md) no backup. Esses componentes têm uma instância [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente no documento componentes de backup. Esses componentes são incluídos em uma restauração usando [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore).
-   Um componente pode ter sido [*incluído implicitamente*](vssgloss-i.md) no backup. Esses componentes não têm uma instância [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente no documento componentes de backup; no entanto, sempre haverá uma instância de **IVssComponent** para algum componente ancestral no documento. Esses componentes são incluídos em uma restauração usando [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).

Qualquer componente que tenha sido explicitamente incluído no backup sempre poderá ser selecionado individualmente para restauração, independentemente de seu valor de seleção para restauração. O solicitante chama [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), passando a ID do gravador, o caminho lógico e o nome do componente específico. Os componentes que foram incluídos implicitamente no backup serão restaurados quando um ancestral explicitamente incluído for restaurado. Os componentes incluídos implicitamente podem ser selecionados individualmente para restauração somente se forem marcados como selecionáveis para restauração. Primeiro, o solicitante chama **IVssBackupComponents:: SetSelectedForRestore** no componente ancestral mais próximo incluído e, em seguida, chama [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) no componente ancestral para selecionar o componente incluído implicitamente para restauração. Depois que isso for feito, somente o componente selecionado implicitamente será restaurado; todos os outros componentes no conjunto de componentes não serão restaurados.

Ao contrário da seleção de backup, que sempre deve ser definida explicitamente quando um componente é adicionado com [**IVssCreateWriterMetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent), a seleção de Restore tem um valor padrão de false, que pode ser substituído.

Como os componentes de nível superior (componentes com um caminho lógico vazio) só podem ser incluídos explicitamente em um backup, a seleção de restauração não tem significado para esses componentes.

 

 



