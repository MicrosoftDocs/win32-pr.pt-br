---
description: Como os arquivos são objetos de segurança, o acesso a eles é regulamentado pelo modelo de controle de acesso que rege o acesso a todos os outros objetos que podem ser Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Segurança de arquivos e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f33df8117debef1d7f8349ae2fb479974e59ec582d7be758a753726706b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696246"
---
# <a name="file-security-and-access-rights"></a>Segurança de arquivos e direitos de acesso

Como os arquivos [são objetos](/windows/desktop/SecAuthZ/securable-objects)de segurança , o acesso a eles é regulamentado pelo modelo de controle de acesso que rege o acesso a todos os outros objetos que podem ser Windows. Para uma explicação detalhada desse modelo, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

Você pode especificar um [descritor de](/windows/desktop/api/winnt/ns-winnt-security_descriptor) segurança para um arquivo ou diretório ao chamar a função [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)ou [**CreateDirectoryEx.**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) Se você especificar **NULL** para o *parâmetro lpSecurityAttributes,* o arquivo ou diretório obtém um descritor de segurança padrão. As listas de controle de acesso (ACL) no descritor de segurança padrão para um arquivo ou diretório são herdadas de seu diretório pai. Observe que um descritor de segurança padrão é atribuído somente quando um arquivo ou diretório é recém-criado e não quando ele é renomeado ou movido.

Para recuperar o descritor de segurança de um objeto de arquivo ou diretório, chame a [**função GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Para alterar o descritor de segurança de um objeto de arquivo ou diretório, chame a [**função SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) ou [**SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

Os direitos de acesso válidos para arquivos e diretórios [](/windows/desktop/SecAuthZ/standard-access-rights)incluem os direitos de acesso padrão **DELETE,** READ **\_ CONTROL,** WRITE **\_ DAC,** WRITE **\_ OWNER** e **SYNCHRONIZE.** A tabela em [**Constantes de Direitos de Acesso a Arquivos**](file-access-rights-constants.md) lista os direitos de acesso específicos para arquivos e diretórios.

Embora o direito de acesso [](/windows/desktop/SecAuthZ/standard-access-rights) **SYNCHRONIZE** seja definido na lista de direitos de acesso padrão como o direito de especificar um alçamento de arquivo em uma das funções de espera, ao usar operações assíncronas de E/S de arquivo, você deve aguardar o alçamento de evento contido em uma estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) configurada corretamente em vez de usar o handle de arquivo com o direito de **acesso SYNCHRONIZE** para sincronização.

A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para arquivos e diretórios.



<table>
<thead>
<tr class="header">
<th>Direito de acesso</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>Sincronizar</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows compara os direitos de acesso solicitados e as informações no token de acesso do thread com as informações no descritor de segurança do arquivo ou do objeto de diretório. Se a comparação não proibir que todos os direitos de acesso solicitados sejam concedidos, um identificador para o objeto será retornado ao thread e os direitos de acesso serão concedidos. Para obter mais informações sobre esse processo, consulte [Interação entre threads e objetos securáveis.](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects)

Por padrão, a autorização para acesso a um arquivo ou diretório é controlada estritamente pelas ACLs no descritor de segurança associado a esse arquivo ou diretório. Em particular, o descritor de segurança de um diretório pai não é usado para controlar o acesso a nenhum arquivo ou diretório filho. O **direito de acesso FILE \_ TRAVERSE** pode ser imposto removendo o **privilégio BYPASS \_ TRAVERSE \_ CHECKING** [dos](/windows/desktop/SecAuthZ/privileges) usuários. [](/windows/desktop/SecAuthZ/access-rights-and-access-masks) Isso não é recomendado no caso geral, pois muitos programas não lidam corretamente com erros de travessia de diretório. O principal uso para o acesso **DE \_ TRAVERSE** de ARQUIVO nos diretórios é habilitar a conformidade com determinados padrões IEEE e ISO POSIX quando a interoperabilidade com sistemas Unix é um requisito.

O Windows de segurança do Windows fornece uma maneira para um diretório filho herdar ou ser impedido de herdar uma ou mais ACEs no descritor de segurança do diretório pai. Cada ACE contém informações que determinam como ela pode ser herdada e se ela terá um efeito no objeto de diretório herdado. Por exemplo, alguns ACEs herdados controlam o acesso ao objeto de diretório herdado e eles são chamados *de ACEs efetivas.* Todas as outras ACEs são chamadas *de ACEs somente herdado.*

O Windows de segurança também impõe a herança automática de ACEs a objetos filho de acordo com as regras [de herança ace](/windows/desktop/SecAuthZ/ace-inheritance-rules). Essa herança automática, juntamente com as informações de herança em cada ACE, determina como as restrições de segurança são passadas para baixo na hierarquia de diretórios.

Observe que você não pode usar uma ACE negada por acesso para negar apenas **acesso GENERIC \_ READ** ou **GENERIC \_ WRITE** a um arquivo. Isso porque, para objetos de arquivo, os mapeamentos genéricos para **LEITURA \_ GENÉRICA** ou **GRAVAÇÃO \_ GENÉRICA** incluem o **direito de acesso SYNCHRONIZE.** Se uma ACE negar acesso **DE \_** GRAVAÇÃO GENÉRICO a um usuário confiável e o usuário confiável solicitar acesso DE LEITURA GENÉRICO, a solicitação falhará porque a solicitação inclui implicitamente o acesso **SYNCHRONIZE,** que é implicitamente negado pela ACE e vice-versa. **\_** Em vez de usar ACEs negadas para acesso, use ACEs permitidas para permitir explicitamente os direitos de acesso permitidos.

Outro meio de gerenciar o acesso a objetos de armazenamento é a criptografia. A implementação da criptografia do sistema de arquivos Windows é o Sistema de Arquivos Criptografado ou EFS. O EFS criptografa apenas arquivos e não diretórios. A vantagem da criptografia é que ela fornece proteção adicional para arquivos que são aplicados na mídia e não por meio do sistema de arquivos e da arquitetura de controle de acesso Windows padrão. Para obter mais informações sobre criptografia de arquivo, consulte [Criptografia de arquivo](file-encryption.md).

Na maioria dos casos, a capacidade de ler e gravar as configurações de segurança de um objeto de arquivo ou diretório é restrita aos processos de modo kernel. Claramente, você não deseja que qualquer processo de usuário seja capaz de alterar a propriedade ou a restrição de acesso em seu arquivo ou diretório privado. No entanto, um aplicativo de backup não poderá concluir seu trabalho de backup do arquivo se as restrições de acesso que você colocou em seu arquivo ou diretório não permitirem que o processo de modo de usuário do aplicativo o leia. Os aplicativos de backup devem ser capazes de substituir as configurações de segurança de objetos de arquivo e diretório para garantir um backup completo. Da mesma forma, se um aplicativo de backup tentar gravar uma cópia de backup do arquivo pela cópia residente em disco e você negar explicitamente privilégios de gravação para o processo de aplicativo de backup, a operação de restauração não poderá ser concluída. Nesse caso, também, o aplicativo de backup deve ser capaz de substituir as configurações de controle de acesso do arquivo.

Os **ES \_ BACKUP NAME \_ e** **os ES acesso RESTORE \_ \_ NAME** foram criados especificamente para fornecer essa capacidade de fazer backup de aplicativos. Se esses privilégios foram concedidos e habilitados no token de acesso do processo de aplicativo de backup, ele pode chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir seu arquivo ou diretório para backup, especificando o direito de acesso **READ \_ CONTROL** padrão como o valor do parâmetro *dwDesiredAccess.* No entanto, para identificar o processo de chamada como um processo de backup, a chamada para **CreateFile** deve incluir o sinalizador **\_ \_ \_ SEMANTICS** DE BACKUP DO SINALIZADOR DE ARQUIVO no parâmetro *dwFlagsAndAttributes.* A sintaxe completa da chamada de função é a seguinte:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Isso permitirá que o processo do aplicativo de backup abra seu arquivo e substitua a verificação de segurança padrão. Para restaurar o arquivo, o aplicativo de backup usaria a sintaxe [**de chamada CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) a seguir ao abrir o arquivo a ser gravado.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Há situações em que um aplicativo de backup deve ser capaz de alterar as configurações de controle de acesso de um arquivo ou diretório. Um exemplo é quando as configurações de controle de acesso da cópia residente em disco de um arquivo ou diretório são diferentes da cópia de backup. Isso ocorreria se essas configurações fossem alteradas após o backup do arquivo ou do diretório ou se ele estivesse corrompido.

O **sinalizador DE \_ \_ \_ SEMÂNTICA DE BACKUP** DO SINALIZADOR DE ARQUIVO especificado na chamada para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) concede permissão ao processo de aplicativo de backup para ler as configurações de controle de acesso do arquivo ou diretório. Com essa permissão, o processo de aplicativo de backup pode chamar [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) para ler e redefinir as configurações de controle de acesso.

Se um aplicativo de backup deve ter acesso às configurações de controle de acesso no nível do [sistema,](/windows/desktop/SecAuthZ/access-control-lists)o sinalizador **ACCESS SYSTEM \_ \_ SECURITY** deve ser especificado no valor do parâmetro *dwDesiredAccess* passado para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Os aplicativos de backup chamam [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) para ler os arquivos e diretórios especificados para a operação de restauração e [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) para escrevê-los.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
