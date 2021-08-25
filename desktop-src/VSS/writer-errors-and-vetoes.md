---
description: Um gravador pode falhar por vários motivos programáticos.
ms.assetid: 50eced73-3917-4d7e-96cc-2d793b448738
title: Erros e Vetações do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0835775aec21da9aa69e81b4f7af63f98d765b5c72763cb52af706c4e7a720e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124456"
---
# <a name="writer-errors-and-vetoes"></a>Erros e Vetações do gravador

Um gravador pode falhar por vários motivos programáticos. Quando isso acontece, ele deve vetar a operação de backup, restauração ou cópia de sombra em andamento chamando o método [**CVssWriter:: SetWriterFailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure) em um dos seus métodos de manipuladores (por exemplo, [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) ou [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) e retornando **true**. Opcionalmente, ele também pode definir uma cadeia de caracteres de mensagem de erro em resposta a uma condição de falha em determinados métodos de manipulador com os métodos [**IVssComponentEx:: SetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setprepareforbackupfailuremsg), [**IVssComponentEx:: SetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg), [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)e [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg) . O solicitante pode aceitar a veto ou continuar com o backup, ignorando a veto.

Um solicitante deve verificar o status do gravador (usando [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)) seguindo cada evento gerado por ele.

Em alguns casos, as mensagens de erro podem ser recuperadas dessas falhas (usando os métodos [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg), [**IVssComponent:: GetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg), [**IVssComponentEx:: GetPostSnapshotFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getpostsnapshotfailuremsg)e [**IVssComponent:: GetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg) ) ou um gravador pode optar por definir os metadados (usando [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata) e [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) com informações de estado de erro). Por exemplo, código que mostra como exibir essas mensagens de erro, consulte [**IVssComponentEx:: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).

Dependendo do estado do erro, um solicitante ou seu operador pode reiniciar o backup e a cópia de sombra com qualquer modificação necessária no estado do trabalho ou do sistema de backup.

Por exemplo, suponha que [**GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) retornou o seguinte:

-   **VSS \_ E \_ WRITERERROR \_ INCONSISTENTSNAPSHOT** sugere que um solicitante pode adicionar volumes adicionais à cópia de sombra
-   **VSS \_ E \_ WRITERERROR com \_ nova tentativa** indica que tentar novamente sem reconfiguração pode funcionar. Se o gravador continuar a retornar o erro após várias tentativas, tente reiniciar o serviço que hospeda o gravador. Os seguintes gravadores estão hospedados no serviço VSS: gravador de registro, gravador de banco de dados de registro de classe COM+, gravador de otimização de cópia de sombra e gravador ASR (recuperação automatizada do sistema). Se o gravador pertencer a um aplicativo que hospeda o gravador em seu próprio processo, tente reiniciar o aplicativo.

    **Windows Server 2003 e Windows XP:** os seguintes gravadores estão hospedados no serviço VSS: gravador de registro, gravador de banco de dados de registro de classe COM+, gravador de log de eventos de aplicativo e Microsoft SQL Server gravador do mecanismo de área de trabalho 2000 (MSDE).

-   \_ \_ O status do VSS e do gravador \_ \_ não \_ disponível indica que um gravador pode ter atingido o número máximo de sessões de backup e restauração disponíveis e tentar novamente pode funcionar quando o sistema está menos ocupado.
-   **VSS \_ E \_ WRITERERROR \_ OUTOFRESOURCES** ou **VSS \_ e \_ WRITERERROR \_ Timeout** podem sugerir que a carga do sistema seja reduzida antes de tentar novamente
-   **VSS \_ E \_ WRITERERROR sem \_ nova tentativa** ou **o \_ gravador E o VSS \_ \_ não \_ responderiam** provavelmente indicando um erro do gravador tão grave quanto para impedir a tentativa de fazer backup de seus dados com o VSS.

Dependendo de qual gravador e quais componentes os geram, nem sempre é necessário que um aplicativo de backup anule após um veto ou erro.

Por exemplo, um solicitante pode decidir que a intenção da cópia de sombra é fazer backup do aplicativo A e a veto foi recebida do gravador para o aplicativo de backup B. Nesse caso, é perfeitamente aceitável continuar a fazer backup do aplicativo a enquanto ignora a veto.

Veja a seguir exemplos de uma veto de gravador:

-   O gravador veta o processo de criação de cópia de sombra quando não conseguiu suspender suas atividades durante o tempo em que a cópia de sombra estava sendo criada. Isso indica que há uma alta probabilidade de que a cópia de sombra não seja válida porque ocorreu uma operação de gravação durante o estado de congelamento.
-   Um aplicativo de backup solicitou uma cópia de sombra do volume C: e um gravador determina que uma cópia de sombra de C: e D: é fazer backup de seus dados. Nesse caso, o gravador será vetado. O aplicativo de backup pode examinar os metadados e determinar se o gravador será ignorado ou se o processo de criação da cópia de sombra será anulado e depois reiniciado.

 

 



