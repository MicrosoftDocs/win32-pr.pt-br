---
description: no Windows Vista e no Windows Server 2008 e posterior, o desenvolvedor de um gravador ou aplicativo VSS pode optar por excluir determinados arquivos das cópias de sombra.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Excluindo arquivos de cópias de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39acf8c92d44bcf8786a880b6ae5eb6a88786809f5af1609dee1b342cd2fb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122099"
---
# <a name="excluding-files-from-shadow-copies"></a>Excluindo arquivos de cópias de sombra

no Windows Vista e no Windows Server 2008 e posterior, o desenvolvedor de um gravador ou aplicativo VSS pode optar por excluir determinados arquivos das cópias de sombra.

O impacto no desempenho e a área de armazenamento de cópia de sombra (também chamada de "área de comparação") o uso de um arquivo em uma cópia de sombra estão diretamente relacionados à quantidade de alterações no conteúdo do arquivo depois que a cópia de sombra é criada. Além disso, a exclusão de arquivos de cópias de sombra pode retardar a criação da cópia de sombra.

Por esses motivos, um arquivo deve ser excluído das cópias de sombra somente se for grande, passa por uma alteração significativa entre uma cópia de sombra e a próxima, e não precisa de backup.

Você só deve excluir arquivos que pertençam ao seu aplicativo.

Se o \_ sinalizador de \_ não-recuperação do VSS VOLSNAP \_ não \_ for definido no contexto de cópia de sombra, isso significará que a recuperação automática está desabilitada e nenhum arquivo pode ser excluído da cópia de sombra. Para obter mais informações, consulte a enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Usando o método AddExcludeFilesFromSnapshot

Um gravador VSS pode excluir arquivos de uma cópia de sombra da seguinte maneira:

1.  Chame o método [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) para relatar os arquivos a serem excluídos.
2.  No método [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) do gravador, exclua os arquivos da cópia de sombra.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Usando a chave do registro FilesNotToSnapshot

> [!Note]  
> A chave do Registro **FilesNotToSnapshot** deve ser usada somente por aplicativos. Os usuários que tentarem usá-lo encontrarão limitações, como as seguintes:
>
> -   Ela não pode excluir arquivos de uma cópia de sombra criada em um Windows Server usando o recurso Versões Anteriores.
> -   Ela não pode excluir arquivos de cópias de sombra para pastas compartilhadas.
> -   Ele pode excluir arquivos de uma cópia de sombra que foi criada usando o utilitário [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , mas não pode excluir arquivos de uma cópia de sombra que foi criada usando o utilitário [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .
> -   Os arquivos são excluídos de uma cópia de sombra com base no melhor esforço. Isso significa que não há garantia de exclusão.

 

Um aplicativo VSS pode excluir arquivos de uma cópia de sombra durante a criação da cópia de sombra usando a seguinte chave do registro:

**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**

Essa chave do registro tem \_ \_ valores de reg multi sz para cada aplicativo cujos arquivos podem ser excluídos. Os arquivos são especificados por caminhos totalmente qualificados, que podem conter o \* curinga.

Em todos os casos, a entrada será ignorada se não houver nenhum arquivo que corresponda à cadeia de caracteres do caminho.

Depois que um arquivo é adicionado ao valor apropriado da chave do registro, ele é excluído da cópia de sombra durante a criação pelo gravador de otimização de cópia de sombra em uma base de melhor esforço.

Se um caminho totalmente qualificado não puder ser especificado, um caminho também poderá ser implícito usando a variável $UserProfile $ ou $AllVolumes $. Por exemplo:

-   Nome de arquivo de subdiretório $UserProfile $ \\ Directory \\ \\ .\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* .\*

Para tornar o caminho recursivo, acrescente "/s" ao final. Por exemplo:

-   Nome de \\ arquivo do subdiretório do $USERPROFILE $ Directory \\ \\ . \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* . \* /s

A variável $UserProfile $ faz com que a cadeia de caracteres do caminho seja aplicada a todos os perfis de usuário no computador. Os perfis de usuário são enumerados examinando a seguinte chave do registro:

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ outfilelist**

A variável $AllVolumes $ faz com que a cadeia de caracteres do caminho seja aplicada a todas as cópias de sombra no computador. Por exemplo, suponha que o caminho seja "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s ", e o computador tem três volumes: C:, D: e E:. Se C: e E: contiver o caminho " \\ TemporaryFiles \\ " e o volume D: contiver apenas o caminho d: \\ Data \\ , a árvore de diretórios C: \\ TemporaryFiles \\ será excluída das cópias de sombra de C:, e a árvore de diretórios e: \\ TemporaryFiles \\ será excluída das cópias de sombra de E:.

Os administradores podem desabilitar a expansão da variável $UserProfile $ usando a seguinte chave do registro:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Services \\ Vss \\ Configurações**

Nessa chave do registro, especifique DisableUserProfileExpansion para o nome do valor, REG \_ DWORD para o tipo de valor e um valor diferente de zero para os dados do valor.

## <a name="about-the-filesnottobackup-registry-key"></a>Sobre a chave do Registro FilesNotToBackup

A chave do registro **FilesNotToBackup** pode ser usada para especificar os nomes dos arquivos e diretórios nos quais os aplicativos de backup não devem fazer backup ou restaurar. No entanto, ele não exclui esses arquivos das cópias de sombra. Para obter mais informações sobre essa chave do registro, consulte [chaves e valores do registro para backup e restauração](../backup/registry-keys-for-backup-and-restore.md).

 

 
