---
description: Pode ser necessário que um serviço seja interrompido antes e reiniciado após uma operação de restauração.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Interrompendo serviços para restauração por solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa8051fc20c5ba1bd930da8c7da5c40829c07772572c2b1fb795250d34b8c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511616"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Interrompendo serviços para restauração por solicitantes

Pode ser necessário que um serviço seja interrompido antes e reiniciado após uma operação de restauração.

Normalmente, parar e iniciar um serviço para dar suporte a uma restauração seria executado por um gravador ao manipular o evento de [*Prerestore*](vssgloss-p.md) (with [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) e o evento [*createrestore*](vssgloss-p.md) (with [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).

No entanto, pode haver casos em que é necessário que um solicitante interrompa explicitamente um serviço em execução. Os gravadores indicam se esse é o caso definindo o \_ valor de inicialização do VSS RME \_ Stop \_ Restore \_ ou do VSS \_ RME \_ Restore \_ Stop \_ da enumeração de [**enumeração do VSS \_ \_ RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) como o argumento do método Restore de uma chamada para o método [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) e especificando o nome do serviço a ser parado.

Um solicitante Obtém informações sobre o método Restore e o nome do serviço a ser interrompido ao trabalhar com metadados do gravador usando o método [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) .

É importante que o gravador, ao especificar o nome de um serviço a ser interrompido, use o nome público correto desse serviço. Um nome ambíguo ou inexato pode fazer com que os solicitantes interrompam o serviço errado ou não conseguirem determinar qual serviço deve ser interrompido.

Após a conclusão da operação de restauração, os solicitantes devem reiniciar o serviço.

Você deve ter cuidado ao projetar e implementar gravadores que dão suporte a serviços que os solicitantes devem parar e reiniciar. Especificamente, esses gravadores não devem realmente fazer parte do serviço, ou seja, o próprio gravador não precisa ser interrompido e reiniciado no decorrer da operação de restauração.

Um gravador cujo processo é interrompido terá uma instância de gravador diferente após a reinicialização. A nova instância do gravador não receberá eventos VSS destinados à instância original do gravador. Especificamente, se o processo de uma instância do gravador for interrompido depois de manipular um evento de pré-restauração, a nova instância não receberá o evento de restauração. Além disso, o VSS gerará um erro indicando a perda de um gravador participante na operação de restauração e [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) pode retornar uma falha.

 

 



