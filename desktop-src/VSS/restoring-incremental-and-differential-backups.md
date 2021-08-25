---
description: A restauração de um backup incremental ou diferencial no VSS não é significativamente diferente de qualquer outra operação de restauração do VSS.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Restaurando backups incrementais e diferenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcc0c2df57e2f7c0f21436248ddaa46231c7bf6440c76a38f4d1c92ab2adf97f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864046"
---
# <a name="restoring-incremental-and-differential-backups"></a>Restaurando backups incrementais e diferenciais

A restauração de um backup incremental ou diferencial no VSS não é significativamente diferente de qualquer outra operação de restauração do VSS.

Um gravador pode modificar destinos de restauração ou direcionamento direcionado a solicitações, e um solicitante deve tratar mapeamentos de local e novos destinos alternativos, assim como acontece com qualquer outra restauração. No entanto, há dois problemas significativos a serem considerados no tratamento da restauração de um backup incremental ou diferencial: restaurações adicionais e carimbos de backup.

## <a name="additional-restores"></a>Restaurações adicionais

A primeira questão é a de restaurações adicionais. Um operador de backup pode precisar executar várias operações de restauração usando uma mídia de backup incremental completa e uma subseqüente, como uma origem.

Alguns gravadores, normalmente como parte de seu manuseio de um evento de [*restauração*](vssgloss-p.md) usando [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), usam arquivos restaurados para realizar atualizações de dados atualmente no disco. Para alguns desses gravadores, ele é ineficiente, ou perigoso, para atualizar repetidamente os dados em disco de arquivos restaurados.

Portanto, é importante que os aplicativos de backup indiquem quando um componente ou conjunto de componentes pode exigir restaurações subsequentes chamando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Um gravador chamaria [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) para determinar se o operador de backup planejou mais restaurações do componente ou conjunto de componentes.

Se o solicitante não tiver chamado [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores), [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) retornará false e o gravador poderá executar qualquer processamento após a restauração necessário.

Se [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) tivesse sido chamado, [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) retorna **true** e um gravador deve decidir como tratar as operações de pós-restauração — por exemplo, o gravador pode optar por não atualizar seus dados em disco.

## <a name="backup-stamps"></a>Carimbos de backup

Como parte da operação de backup completo anterior, um gravador pode ter armazenado um carimbo de backup no documento de componentes de backup do solicitante.

O carimbo de backup é armazenado como uma cadeia de caracteres, e seu formato e informações não são compreensíveis para o solicitante. Portanto, o solicitante não pode fazer uso direto das informações de carimbo de backup.

Em vez disso, sua tarefa é tornar essas informações disponíveis para o gravador, chamando o método [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) antes da geração de um evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para um backup incremental.

O solicitante faz isso em uma base componente por componente. Um solicitante examina o componente armazenado ou o conjunto de componentes informações de carimbo de backup usando [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Se as informações de carimbo de backup forem apropriadas para o tipo de restauração que o solicitante está realizando, ela a disponibilizará como carimbo de data/hora do último backup de um componente com o método [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) .

Um gravador recupera as informações de carimbo de backup usando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Um gravador dessa classe gerou o carimbo de backup inicial, portanto, o gravador é capaz de decodificar esse carimbo e usar as informações. Com base nele, ao manipular um evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , um gravador pode optar por executar ações como alterar destinos de restauração ou solicitar direcionamento direcionado.

 

 



