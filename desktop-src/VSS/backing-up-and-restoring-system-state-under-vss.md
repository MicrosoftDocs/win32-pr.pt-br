---
description: Observação Este tópico se aplica somente ao Windows Server 2003 R2 e ao Windows Server 2003 com Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Fazendo backup e restaurando o estado do sistema no Windows Server 2003 R2 e no Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922718"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>Fazendo backup e restaurando o estado do sistema no Windows Server 2003 R2 e no Windows Server 2003 SP1

> [!Note]  
> Este tópico se aplica somente ao Windows Server 2003 R2 e ao Windows Server 2003 com Service Pack 1 (SP1). Para obter informações sobre outras versões de sistema operacional, consulte [fazendo backup e restaurando o estado do sistema](locating-additional-system-files.md).

 

> [!Note]  
> A Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online no Windows (todas as versões). Para obter informações sobre como usar as APIs e os procedimentos fornecidos pela Microsoft para implementar restaurações de estado do sistema online, consulte os recursos da Comunidade disponíveis no [msdn Community Center](https://msdn.microsoft.com/community/default.aspx).

 

Ao executar um backup ou restauração do VSS, o estado do sistema do Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos. Esses elementos sempre devem ser tratados por operações de backup e restauração como uma unidade.

No Windows Server 2003 R2 e no Windows Server 2003 com SP1, não há nenhuma API do Windows criada para tratar esses objetos como um, portanto, é recomendável que os solicitantes tenham seu próprio objeto de estado do sistema para que possam processar esses componentes de forma consistente.

Como o VSS é executado em versões do Windows em que o WFP ( [*proteção de arquivo do sistema*](vssgloss-s.md) ) protege os arquivos de estado do sistema contra corrupção, são necessárias etapas especiais para fazer backup e restaurar o estado do sistema.

O estado do sistema consiste no seguinte:

-   Todos os arquivos protegidos por WFP, arquivos de inicialização, incluindo NTLDR, NTDETECT e configurações de contador de desempenho
-   O Active Directory (ADSI) (em sistemas que são controladores de domínio)
-   A pasta de volume do sistema (SYSVOL) que é replicada pelo FRS (serviço de replicação de arquivo) (em sistemas que são controladores de domínio)
-   Servidor de certificado (em sistemas que fornecem autoridade de certificação)
-   Banco de dados de cluster (em sistemas que são um nó de um cluster do Windows)
-   Serviço de Registro
-   Banco de dados de registro de classe COM+

O backup do estado do sistema pode ser feito em qualquer ordem.

No entanto, a restauração do estado do sistema deve substituir os arquivos de inicialização primeiro e confirmar a seção do sistema (Hive) do registro como uma etapa final no processo e pode ocorrer na seguinte ordem:

1.  Restaure os arquivos de inicialização.
2.  Banco de dados de registro de classe COM+
3.  Restaurar SYSVOL, servidor de certificado e bancos de dados de cluster (se necessário).
4.  Restaurar Active Directory (se necessário).
5.  Restaure o registro.

Alguns serviços do sistema, como a autoridade de certificação, têm gravadores VSS convencionais e seguem os algoritmos de backup e restauração do VSS. Outros, como o registro, exigem operações de backup ou restauração personalizadas; para obter mais informações, consulte [backups e restaurações personalizadas](custom-backups-and-restores.md).

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Backup e restaurações do VSS de arquivos de inicialização e do sistema

Os arquivos de inicialização e de sistema devem ser armazenados em backup e restaurados somente como uma única entidade.

Um solicitante pode usar com segurança as versões de cópia de sombra desses arquivos e deve ter certeza de que o volume do sistema e o dispositivo de inicialização sejam [*copiados em sombra*](vssgloss-s.md).

Os arquivos do sistema e de inicialização incluem:

-   Os principais arquivos de inicialização: <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (se presente)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% \\ System32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Todos os arquivos protegidos pela [*proteção de arquivo do sistema*](vssgloss-s.md) e enumerados pelo [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (consulte operações de restauração do VSS de arquivos protegidos por WFP) -   os arquivos de configuração do contador de desempenho: <dl> % SystemRoot% \\ System32 \\ perf? 00?. DATs  
    % SystemRoot% \\ System32 \\ perf? 00?. Bak </dl>
-   Se estiver presente, o arquivo da metabase do IIS (servidor de informações da Internet) deverá ser incluído nas operações de backup e restauração porque ele contém o estado usado pelo Microsoft Exchange e outros aplicativos de rede. Esse arquivo pode ser encontrado em: <dl> % SystemRoot% \\ System32 \\ inetsrv \\ metabase. bin </dl>
-   Se o backup do arquivo da metabase do IIS for feito, as chaves para permitir que os aplicativos leiam determinadas entradas criptografadas devem ser restauradas como parte do estado do sistema. Os arquivos podem ser encontrados em: <dl> % SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
    % AllUsersProfile% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\* </dl>
-Ao fazer backup de arquivos de inicialização e do sistema, pode ser necessário determinar o dispositivo de inicialização do dos fazendo o seguinte: 1. localize a partição do sistema em **HKEY \_ local \_ Machine** \\ **System** \\ **Setup** \\ **SystemPartition**.
    2.  Passar a variável de ambiente raiz do sistema (% SystemRoot%) para o Gerenciador de montagem para obter o nome do dispositivo NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Operações de restauração do VSS de arquivos protegidos por WFP

O serviço WFP foi projetado para impedir a substituição acidental ou gradual de arquivos do sistema. Portanto, etapas especiais precisam ser executadas para restaurar dados WFP.

O significa que o gravador WFP deve especificar o método de restauração do **VSS \_ RME \_ \_ na \_ reinicialização** ao definir seu documento de metadados do gravador. Se um solicitante determinar que o gravador WFP falhou ao especificar esse método de restauração, ele indicará um erro de gravador.

Um solicitante deve implementar um método de restauração do **VSS \_ RME \_ Restore \_ na \_ reinicialização** usando a função do Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) com o **atraso de MoveFile até o parâmetro \_ \_ \_ reboot** para substituir os arquivos do sistema. Os arquivos restaurados não são copiados para os diretórios de arquivo do sistema real até após a reinicialização do sistema. A substituição de arquivos protegidos do sistema ocorrerá somente se o valor da seguinte entrada de registro do **reg \_ Word** for definido como 1:

**HKEY \_ \_** Gerenciador de sessão de controle CurrentControlSet do sistema de máquina local \\  \\  \\  \\  \\ **AllowProtectedRenames** = 1

Esse valor deve ser definido antes de qualquer inicialização em que os arquivos protegidos sejam substituídos via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e são excluídos após a reinicialização.

O diretório dllcache do sistema também deve ser submetido a backup ou restaurado, com backup e restauração do volume de inicialização, e está localizado examinando a entrada de registro **reg \_ Expand \_ sz** :

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ expande \_ sz</dd> </dl>

O conteúdo do diretório dllcache do sistema é recriado usando o verificador de arquivos do sistema (SFC) no prompt de comando:

-   A opção **/SCANONCE** examina todos os arquivos protegidos na próxima inicialização do sistema.
-   A opção **/scannow** examina todos os arquivos protegidos imediatamente.

Todos os arquivos protegidos serão verificados e todas as versões que não forem válidas serão substituídas no diretório e no local de dllcache.

Há quatro arquivos que fazem parte da WFP que não podem ser restaurados com os arquivos WFP:

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Esses arquivos ajudam no processo de restauração dos arquivos WFP e, como tal, há uma dependência circular. Atualmente, não há como restaurar esses arquivos, exceto para reinstalar o Windows.

 

 
