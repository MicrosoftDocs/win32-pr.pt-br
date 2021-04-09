---
description: Veja a seguir dicas para interoperar corretamente com vários sistemas de arquivos e recursos de segurança que foram introduzidos no Windows Vista e no Windows Server 2008.
ms.assetid: 3e8a1fd2-59e5-4f18-aafc-0ce5ac1e1cfa
title: Trabalhando com recursos de segurança e sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12903599beb7ed153965f4b803ad8147fd32067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090432"
---
# <a name="working-with-file-system-and-security-features"></a>Trabalhando com recursos de segurança e sistema de arquivos

Veja a seguir dicas para interoperar corretamente com vários sistemas de arquivos e recursos de segurança que foram introduzidos no Windows Vista e no Windows Server 2008.

## <a name="interoperability-with-transactions"></a>Interoperabilidade com transações

Para dar suporte a transações, o VSS garante que o KTM (kernel Transaction Manager) e o Coordenador de Transações Distribuídas (DTC) estejam congelados antes da criação de cópias de sombra de volume. Se o sistema falhar ao congelar ou descongelar o KTM ou o DTC, os erros de tempo limite a seguir poderão ser retornados pelo método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) :

<dl> \_ \_ \_ tempo limite de congelamento da transação E VSS \_  
\_ \_ \_ tempo limite de descongelar da transação E \_ VSS  
</dl>

Se o solicitante receber um desses códigos de erro, ele deverá repetir a criação da cópia de sombra.

As operações de registro e sistema de arquivos também podem ser transacionadas. No caso do registro, o gravador do registro é responsável por garantir a consistência transacional. No caso de operações do sistema de arquivos NTFS transacionais (TxF), o provedor do sistema é responsável por garantir a consistência transacional. Isso é feito com a montagem da cópia de sombra como leitura/gravação depois que ela é criada para permitir a recuperação automática. Durante a fase de recuperação automática, o KTM reverte todas as transações incompletas.

## <a name="identifying-and-creating-hard-links"></a>Identificando e criando links físicos

Ao fazer backup de arquivos, um aplicativo de backup deve identificar todos os links físicos de cada arquivo para evitar o backup do mesmo arquivo mais de uma vez. Duas novas funções estão disponíveis para enumerar links físicos: [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew).

Da mesma forma, ao restaurar arquivos, o aplicativo de backup deve restaurar links físicos usando a função [**CreateHardLink**](/windows/win32/api/winbase/nf-winbase-createhardlinka) .

Os aplicativos de backup também devem declarar o \_ privilégio de nome de backup se \_ durante a fase de backup e o \_ nome de restauração se \_ durante a fase de restauração.

## <a name="permissions-and-privileges-required-by-backup-applications"></a>Permissões e privilégios exigidos pelos aplicativos de backup

Os aplicativos de backup que restauram arquivos do sistema exigem os seguintes privilégios:

<dl> \_nome do backup se \_  
\_nome de restauração do se \_  
\_nome de segurança se \_  
SE \_ obter \_ nome de propriedade \_  
</dl>

Os aplicativos de backup também devem solicitar \_ direitos de acesso de proprietário de gravação durante a fase de restauração.

## <a name="windows-media-digital-rights-management"></a>Rights Management digital do Windows Media

O cliente Windows Media Digital Rights Management (DRM) mantém um diretório de arquivos de estado e licença confidenciais no diretório% ProgramData% \\ Microsoft \\ Windows \\ DRM. Os arquivos nesse diretório devem ser limpos ao mesmo tempo que arquivos temporários e de cache. Para garantir que o cliente DRM do Windows permaneça em um estado consistente, você deve evitar fazer backup ou restaurar esses arquivos. Esse diretório está listado na chave do Registro FilesNotToBackup. Para obter mais informações sobre a chave FilesNotToBackup, consulte [gerando um conjunto de backup](generating-a-backup-set.md).

## <a name="user-account-control"></a>Controle de Conta de Usuário

A introdução do UAC (controle de conta de usuário) no Windows Vista significa que, a menos que especificado de outra forma, os aplicativos devem ser executados em uma conta de usuário padrão. Além disso, o recurso de virtualização de arquivo e registro do UAC altera os locais onde os dados do usuário são armazenados. Para obter mais informações sobre como trabalhar com o UAC e a virtualização de arquivo e registro, consulte as seguintes referências:

<dl>

[A história do desenvolvedor do Windows Vista e do Windows Server 2008: requisitos de desenvolvimento de aplicativos do Windows Vista para UAC (controle de conta de usuário)](/previous-versions/aa905330(v=msdn.10))  
[Requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10))  
[Aplicação de patch de UAC (controle de conta de usuário)](../msi/user-account-control--uac--patching.md)  
</dl>

## <a name="bitlocker-drive-encryption"></a>Criptografia de Unidade de Disco BitLocker

Criptografia de Unidade de Disco BitLocker é um novo recurso do Windows Vista Enterprise, do Windows Vista Ultimate e do Windows Server 2008 que oferece inicialização segura e criptografia de volume completo. Entender esse recurso é importante para desenvolvedores de aplicativos de backup que executam restaurações offline, onde os dados podem precisar ser restaurados em uma unidade criptografada.

Para restaurar dados em uma unidade criptografada, execute as seguintes etapas:

1.  Desbloqueie a unidade.
2.  Desative Criptografia de Unidade de Disco BitLocker.
3.  Execute a restauração.
4.  Inicialize no sistema operacional restaurado e ative Criptografia de Unidade de Disco BitLocker.

Para obter informações detalhadas sobre Criptografia de Unidade de Disco BitLocker, incluindo um guia passo a passo, consulte [criptografia de unidade de disco BitLocker](https://www.microsoft.com/technet/windowsvista/security/bitlockr.mspx) no site do Microsoft TechNet Windows Vista. Para obter informações sobre o provedor WMI Criptografia de Unidade de Disco BitLocker, consulte [criptografia de unidade de disco BitLocker Provider](../secprov/bitlocker-drive-encryption-provider.md).

 

 
