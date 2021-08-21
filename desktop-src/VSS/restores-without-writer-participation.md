---
description: A participação do gravador em um backup do VSS foi projetada para permitir que os aplicativos controlem o que e como seus dados de restauração serão usados.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Restaura sem participação no gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896cbe81a2c3487bb00b01379b6b5bbe4760ecbb28c1bf94c661eeb0049a3d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056364"
---
# <a name="restores-without-writer-participation"></a>Restaura sem participação no gravador

A participação do gravador em um backup do VSS foi projetada para permitir que os aplicativos controlem o que e como seus dados de restauração serão usados.

Em geral, se um gravador estiver disponível em um sistema, nunca será aconselhável restaurar os dados para seu local original sem a participação do gravador. Essa restauração provavelmente encontraria arquivos de destino bloqueados e executaria um risco significativo de corromper dados.

No entanto, há motivos pelos quais um aplicativo de backup pode querer ou precisa restaurar um backup do VSS sem a participação do gravador:

-   Os dados são gerenciados por aplicativos sem reconhecimento de VSS. Quase todos os sistemas terão alguns aplicativos – editores de texto, leitores de email, processadores de texto e assim por diante, que não têm reconhecimento de VSS. Esses dados não podem ser restaurados usando a participação no gravador.

    Em geral, esse tipo de dados não é crítico para o sistema ou serviço, e restaurá-lo não deve ser problemático ou, pelo menos, não mais problemático do que durante uma restauração convencional.

    Assim como no caso de preparação para restaurações convencionais, se possível, os operadores de restauração devem tentar suspender ou encerrar esses aplicativos antes de iniciar uma restauração do VSS.

-   Gravadores VSS ausentes. Essa situação pode ser bastante comum ao restaurar o estado de um sistema danificado. Uma operação de backup deve determinar se é desejável restaurar arquivos para gravadores ausentes. Se a restauração for desejável, os arquivos poderão ser restaurados assim que um backup convencional os restaurar.
-   Uma restauração privada dos dados de um gravador. Um solicitante pode optar por restaurar os dados de um gravador em execução para algum local privado sem notificar o gravador. Um exemplo disso pode ser a restauração dos dados do gravador para dar suporte à comparação offline. Nesse tipo de situação, um solicitante não desejaria usar o [*novo local de destino*](vssgloss-n.md) ao fazer a restauração, pois não quer que o gravador acesse os dados.
-   Um gravador não deseja estar envolvido durante A restauração. Um gravador indica isso passando \_ o VSS WRE \_ nunca para o parâmetro *writerRestore* de [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Um gravador requer um método de restauração personalizado. Um gravador indica que requer uma restauração personalizada passando no VSS \_ RME \_ personalizado para o parâmetro de *método* de [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod). Nesse caso, esse gravador não deve estar envolvido no processo de restauração, a menos que a documentação de restauração personalizada para esse gravador indique o contrário.

Um solicitante envolve um gravador no processo de restauração especificando um dos componentes do escritor em uma chamada para [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). Os dados de um gravador podem ser restaurados sem envolver o gravador simplesmente não especificando nenhum dos componentes do escritor em uma chamada para **IVssBackupComponents:: SetSelectedForRestore**. Se um gravador não esperar nenhum evento de restauração, envolver esse gravador no processo de restauração poderá fazer com que erros falsos sejam relatados para esse gravador.

 

 



