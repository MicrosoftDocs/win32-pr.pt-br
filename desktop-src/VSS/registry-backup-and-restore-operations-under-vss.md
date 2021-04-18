---
description: O serviço registro do Windows dá suporte a um gravador VSS, chamado de gravador de registro, que permite aos solicitantes fazer backup de um registro do sistema usando dados armazenados em um volume copiado de sombra.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Operações de backup e restauração do registro no VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781485"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Operações de backup e restauração do registro no VSS

O serviço registro do Windows dá suporte a um gravador VSS, chamado de gravador de registro, que permite aos solicitantes fazer backup de um registro do sistema usando dados armazenados em um volume copiado de sombra. Para obter mais informações sobre o gravador do registro, consulte [gravadores VSS in-box](in-box-vss-writers.md).

O gravador do registro executa backups e restaurações in-loco do registro. Além disso, o gravador do registro relata apenas hives do sistema; Ele não relata hives de usuário.

**Windows Server 2003:** O gravador do registro usa um arquivo de repositório intermediário (também conhecido como um arquivo saliva) para armazenar dados de registro. Além disso, o gravador do registro relata hives do sistema e hives do usuário.

A ID do gravador para o gravador do registro é AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP:** Não há nenhum gravador de registro. Os dados do registro são relatados pelo gravador de estado inicializável, cuja ID do gravador é F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.

> [!Note]  
> A Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online no Windows (todas as versões). Para obter informações sobre como usar as APIs e os procedimentos fornecidos pela Microsoft para implementar restaurações de estado do sistema online, consulte os recursos da Comunidade disponíveis no [msdn Community Center](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> As informações a seguir se aplicam somente ao Windows Server 2003 e ao Windows XP.

 

## <a name="registry-backup-using-vss"></a>Backup do registro usando VSS

O gravador do registro exportará e salvará os arquivos de registro ativos nos locais definidos pela chave **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**.

Os nomes dos valores nessa entrada de registro identificam o hive do registro a ser salvo e os dados do valor fornecem o arquivo que contém o arquivo (o arquivo do hive). Os arquivos do hive são especificados com o seguinte formato: \\ dispositivo \\ *HarddiskVolumeX* \\ *caminho* \\ *nome do arquivo*.

Por exemplo, em **HKEY \_ local \_ máquina** \\ **sistema** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**, você pode ver o dispositivo de **\\ \\ \\ software computador de registro**  =  \\ \\ HarddiskVolume1 \\ Windows \\ System32 \\ config \\ software.

O gravador do registro garante que os arquivos do hive sejam salvos em disco antes da sua cópia de sombra.

Ao fazer backup dos hives do registro, um solicitante substituiria o \\ dispositivo \\ *HarddiskVolumeX* pela cadeia de caracteres do [*objeto de dispositivo*](vssgloss-d.md) da cópia de sombra do volume.

> [!Note]  
> Você pode converter o \\ caminho do dispositivo \\ *HarddiskVolumeX* para um caminho Win32 equivalente usando a função [**QueryDosDevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) . Para obter mais informações, consulte [obtendo um nome de arquivo de um identificador de arquivo](../memory/obtaining-a-file-name-from-a-file-handle.md) ou [exibindo nomes de caminho de volume](../fileio/displaying-volume-paths.md).

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Restauração do registro usando APIs do Win32 não VSS

Para uma restauração online (modo de segurança ou sistema operacional completo), as subchaves na chave de registro **HKEY \_ local \_** \\ **System sistema** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **PendingFileRenameOperations** devem ser preservadas.

As funções [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) usam essa chave do registro para armazenar informações sobre os arquivos que foram renomeados usando o atraso de MoveFile até o \_ valor de \_ \_ reinicialização no parâmetro *dwFlags* .

Para preservar o conteúdo da chave do registro **PendingFileRenameOperations** , o aplicativo de backup deve chamar a função [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) para conectar o arquivo do registro a ser restaurado no registro ativo. O aplicativo de backup pode usar as várias funções de registro para copiar as chaves e os valores desejados no hive carregado. Após a conclusão da cópia, as funções [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) e [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) devem ser chamadas.

Para uma restauração offline (ambiente de recuperação do Windows ou Windows PE), não é necessário respeitar a chave do registro **PendingFileRenameOperations** .

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Restauração do registro usando APIs do Win32 não VSS no Windows Server 2003

> [!Note]  
> As informações a seguir se aplicam somente a operações de restauração relacionadas à recuperação de desastre (também conhecida como recuperação bare-metal) que são executadas no Windows Server 2003.

 

Ao restaurar o registro, um aplicativo de backup precisa mover algumas das subchaves do registro atual para o registro que deve ser restaurado.

Para fazer isso, um aplicativo de backup pode chamar **RegLoadKey** para conectar o arquivo do registro a ser restaurado para o registro ativo no momento. Em seguida, ele pode usar as várias funções de registro para copiar as chaves e os valores desejados no hive carregado. Depois que a cópia for concluída, **RegFlushKey** e **RegUnloadKey** serão chamados.

Há uma chave do registro que indica a um aplicativo de restauração (solicitante) as chaves do registro em **HKEY \_ local \_ Machine \\ System** que não devem ser substituídas no momento da restauração:

**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

Parte do processo de restauração de estado do sistema envolve a restauração de um registro de backup anterior.

Os aplicativos de backup precisam tomar cuidado especial ao restaurar o hive do **\_ \_ \\ sistema de máquina local hKey** , pois o processo de instalação de uma versão temporária do sistema operacional Windows terá estabelecido chaves no hive do sistema recém-instalado, cujos valores devem sobreviver à operação de restauração.

Por exemplo, quando o sistema de substituição tiver uma placa de interface de rede diferente do sistema original, a restauração das chaves originais para o cartão anterior resultará em resultados imprevisíveis. Isso ocorre porque o serviço de Plug and Play detectou e colocou entradas apropriadas de registro de serviço e driver no registro. Esses valores devem ser preservados para uma inicialização adequada após a restauração do sistema.

Esta seção descreve como os aplicativos de backup podem descobrir quais chaves e arquivos devem ser preservados ao executar uma restauração do hive do **\_ \_ \\ sistema de máquina local hKey** . Em alguns casos, isso envolverá a cópia programática das chaves do hive de instalação recém instalado para o hive a ser restaurado. Em outros casos, garantir que as chaves do registro de um produto não sejam substituídas é tão simples quanto especificar essas chaves no arquivo de configuração INF do produto.

Chaves (e dados de chave) que devem ser preservadas são enumeradas no hive do **\_ \_ \\ sistema de máquina local hKey** no

**HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

chave como conjuntos de \_ \_ cadeias de caracteres reg multi sz (chamadas de *cadeias de caracteres de chave* neste documento).

Um aplicativo de backup (solicitante) deve examinar os valores dessas chaves no registro ativo e o registro recém restaurado, pois qualquer aplicativo ou serviço pode adicionar valores a qualquer momento.

Como as principais cadeias de caracteres devem ser interpretadas por aplicativos de backup são determinadas pelo caractere de terminal:

1.  As cadeias de caracteres-chave terminadas com uma barra invertida (' \\ ') são interpretadas como subchaves. Quando tal subcadeia de caracteres é encontrada, o aplicativo de backup deve preservar todos os dados e todas as chaves subordinadas.

    Por exemplo, o seguinte especifica que todas as chaves subordinadas e os dados serão preservados em uma operação de restauração:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ dmio \\ informações de inicialização\\**

    Para esse fim, essa chave e todas as chaves e os dados subordinados devem ser copiados do registro existente (ou seja, aquele criado pela instalação do Windows) no registro recém restaurado. Isso é chamado de operação de *substituição de chave* . Essa operação substitui a chave correspondente no Registro restaurado.

2.  As cadeias de caracteres-chave cujo caractere de terminação é um asterisco (' \* ') especifica que todas as subchaves devem ser mescladas. Por exemplo, a cadeia de caracteres chave:

    **HKEY \_ \_Sistema de computador local \\ \\ CurrentControlSet \\ \\ \* Serviços* _

    Especifica que a chave de serviços no registro existente (por exemplo, as criadas pela instalação do Windows) deve ser mesclada no Registro restaurado. Isso é chamado de _key operação Merge * e, se existir uma subchave no hive existente e no hive restaurado, a chave no diretório restaurado será preservada com as seguintes exceções:

    -   Se a subchave no hive existente contiver um valor chamado "Start", e a subchave no restaurada não.
    -   Se a subchave no hive existente e no que foi restaurado contiver um valor chamado "Start", e seu valor numérico no hive existente for menor.

    O valor "Start" no registro especifica quando um serviço ou driver será iniciado e pode ter um valor numérico de 0-4. Quanto menor o valor, mais cedo no processo de inicialização o serviço será iniciado.

    Se essa chave existir nos diretórios existente e restaurado, você deverá examinar o valor da chave inicial em cada Hive. Se o valor no hive existente for menor que o valor no diretório restaurado, o valor mais baixo deverá ser preservado.

    Mais uma vez, essa chave é usada para determinar se um serviço ou driver deve ser iniciado no momento da inicialização, na hora do sistema, manualmente, automaticamente ou desabilitado. O valor mais baixo representa uma hora de início anterior. A hora de início anterior deve ser aplicada ao novo registro para garantir que o serviço ou os drivers sejam iniciados corretamente na próxima inicialização.

3.  As cadeias de caracteres-chave cujo caractere de término não é uma barra invertida nem um asterisco são interpretados como valores do registro a serem preservados.

    Por exemplo, a cadeia de caracteres chave:

    **HKEY \_ local \_ Machine \\ sistema \\ CurrentControlSet \\ Control \\ Session Manager \\ PendingFileRenameOperations**

    O mecanismo pelo qual as chaves podem ser preservadas programaticamente envolve a API do registro do Win32. Por exemplo, um algoritmo é enumerado abaixo:

    1.  Restaure o arquivo do hive do sistema com backup em um arquivo. Para este exemplo, deixe o nome ser System. reg.
    2.  Use **RegLoadKey** para carregar System. reg em **HKEY \_ local \_ Machine** com um nome temporário. Por exemplo, um desses nomes pode ser

        **HKEY \_ \_ computador local \\ tmp \_ System**

    3.  Enumere os valores na subchave **KeysNotToRestore** de ambas as cópias do registro e crie um superconjunto das listas. Copiar cada chave desse tipo existente

        **HKEY \_ \_ computador local \\ System**

        chave para o

        **HKEY \_ \_ computador local \\ tmp \_ System**

        chave de acordo com a semântica descrita acima.

    4.  Ao concluir, use os pontos de entrada do **RegFlushKey**  &  **RegUnloadKey** para salvar o

        **HKEY \_ \_ computador local \\ tmp \_ System**

        Volte para System. reg.

    5.  Por fim, use **RegReplaceKey** para especificar que System. reg é substituir o

        **HKEY \_ \_ computador local \\ System**

        arquivo do hive, sistema.

 

 
