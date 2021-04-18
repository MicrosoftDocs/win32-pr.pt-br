---
description: Como os arquivos são objetos protegíveis, o acesso a eles é regulamentado pelo modelo de controle de acesso que governa o acesso a todos os outros objetos protegíveis no Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Segurança de arquivo e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764698"
---
# <a name="file-security-and-access-rights"></a>Segurança de arquivo e direitos de acesso

Como os arquivos são [objetos protegíveis](/windows/desktop/SecAuthZ/securable-objects), o acesso a eles é regulamentado pelo modelo de controle de acesso que governa o acesso a todos os outros objetos protegíveis no Windows. Para obter uma explicação detalhada desse modelo, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).

Você pode especificar um [descritor de segurança](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para um arquivo ou diretório ao chamar a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)ou [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) . Se você especificar **NULL** para o parâmetro *lpSecurityAttributes* , o arquivo ou diretório obterá um descritor de segurança padrão. As listas de controle de acesso (ACL) no descritor de segurança padrão para um arquivo ou diretório são herdadas de seu diretório pai. Observe que um descritor de segurança padrão é atribuído somente quando um arquivo ou diretório é criado recentemente, e não quando é renomeado ou movido.

Para recuperar o descritor de segurança de um objeto de arquivo ou de diretório, chame a função [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Para alterar o descritor de segurança de um objeto de arquivo ou de diretório, chame a função [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) ou [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Os direitos de acesso válidos para arquivos e diretórios incluem os direitos de acesso de **exclusão**, **\_ controle de leitura**, **gravação de \_ DAC**, **\_ proprietário de gravação** e **sincronização** [padrão](/windows/desktop/SecAuthZ/standard-access-rights). A tabela em [**constantes de direitos de acesso**](file-access-rights-constants.md) a arquivos lista os direitos de acesso específicos aos arquivos e diretórios.

Embora o direito de acesso de **sincronização** seja definido na lista de [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) como a direita para especificar um identificador de arquivo em uma das funções de espera, ao usar operações de e/s de arquivo assíncrono, você deve aguardar o identificador de evento contido em uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) configurada corretamente em vez de usar o identificador de arquivo com o direito de sincronização de acesso para **sincronizar** .

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
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SYNCHRONIZE</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

O Windows compara os direitos de acesso solicitados e as informações no token de acesso do thread com as informações no descritor de segurança do objeto de diretório ou arquivo. Se a comparação não proibir a concessão de todos os direitos de acesso solicitados, um identificador para o objeto será retornado ao thread e os direitos de acesso serão concedidos. Para obter mais informações sobre esse processo, consulte [interação entre threads e objetos protegíveis](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

Por padrão, a autorização para acesso a um arquivo ou diretório é controlada estritamente pelas ACLs no descritor de segurança associado a esse arquivo ou diretório. Em particular, o descritor de segurança de um diretório pai não é usado para controlar o acesso a qualquer arquivo ou diretório filho. O [direito de acesso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) de **\_ atravessamento de arquivo** pode ser imposto removendo o [privilégio](/windows/desktop/SecAuthZ/privileges) de **ignorar a \_ \_ verificação** de desvio dos usuários. Isso não é recomendado no caso geral, pois muitos programas não manipulam corretamente erros de percurso de diretório. O uso principal para o direito de acesso ao **arquivo \_ atravessa** os diretórios é habilitar a conformidade para determinados padrões de POSIX IEEE e ISO quando a interoperabilidade com sistemas UNIX é um requisito.

O modelo de segurança do Windows fornece uma maneira para que um diretório filho herde ou seja impedido de herdar, uma ou mais das ACEs no descritor de segurança do diretório pai. Cada ACE contém informações que determinam como ela pode ser herdada e se ela terá um efeito no objeto herdado de diretório. Por exemplo, algumas ACEs herdadas controlam o acesso ao objeto de diretório herdado, e elas são chamadas de *ACEs efetivas*. Todas as outras ACEs são chamadas *de ACEs somente herdadas*.

O modelo de segurança do Windows também impõe a herança automática de ACEs para objetos filho de acordo com as [regras de herança da ACE](/windows/desktop/SecAuthZ/ace-inheritance-rules). Essa herança automática, juntamente com as informações de herança em cada ACE, determina como as restrições de segurança são passadas para baixo na hierarquia de diretório.

Observe que você não pode usar uma ACE com acesso negado para negar somente a **\_ leitura genérica** ou somente o acesso de **\_ gravação genérico** a um arquivo. Isso ocorre porque, para objetos de arquivo, os mapeamentos genéricos **para \_ leitura genérica** ou **\_ gravação genérica** incluem o direito de acesso **sincronizar** . Se uma ACE negar acesso **de \_ gravação genérico** a um confiável e o acesso de **\_ leitura genérico** das solicitações de confiança, a solicitação falhará porque a solicitação inclui implicitamente o acesso de **sincronização** , que é negado implicitamente pela Ace e vice-versa. Em vez de usar ACEs com acesso negado, use ACEs de acesso permitido para permitir explicitamente os direitos de acesso permitidos.

Outro meio de gerenciar o acesso a objetos de armazenamento é a criptografia. A implementação da criptografia do sistema de arquivos no Windows é o sistema de arquivos criptografado, ou EFS. O EFS criptografa apenas arquivos e não diretórios. A vantagem da criptografia é que ela fornece proteção adicional aos arquivos que são aplicados na mídia e não ao sistema de arquivos e à arquitetura de controle de acesso padrão do Windows. Para obter mais informações sobre criptografia de arquivo, consulte [criptografia de arquivo](file-encryption.md).

Na maioria dos casos, a capacidade de ler e gravar as configurações de segurança de um objeto de arquivo ou diretório é restrita a processos de modo kernel. Claramente, você não desejaria que nenhum processo de usuário pudesse alterar a propriedade ou a restrição de acesso em seu arquivo ou diretório particular. No entanto, um aplicativo de backup não poderá concluir seu trabalho de fazer backup de seu arquivo se as restrições de acesso que você colocou em seu arquivo ou diretório não permitirem que o processo de modo de usuário do aplicativo o leia. Os aplicativos de backup devem ser capazes de substituir as configurações de segurança dos objetos de arquivo e de diretório para garantir um backup completo. Da mesma forma, se um aplicativo de backup tentar gravar uma cópia de backup do arquivo na cópia residente em disco e negar explicitamente os privilégios de gravação para o processo do aplicativo de backup, a operação de restauração não poderá ser concluída. Nesse caso também, o aplicativo de backup deve ser capaz de substituir as configurações de controle de acesso do arquivo.

Os privilégios de acesso de nome de **backup do se \_ \_** e se foram criados especificamente para fornecer essa capacidade de fazer backup de aplicativos. **\_ \_** Se esses privilégios tiverem sido concedidos e habilitados no token de acesso do processo do aplicativo de backup, ele poderá chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir o arquivo ou diretório para backup, especificando o direito de acesso **\_ controle de leitura** padrão como o valor do parâmetro *dwDesiredAccess* . No entanto, para identificar o processo de chamada como um processo de backup, a chamada para **CreateFile** deve incluir o sinalizador de semântica de  backup de sinalizador de arquivo no parâmetro dwFlagsAndAttributes. **\_ \_ \_** A sintaxe completa da chamada de função é a seguinte:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Isso permitirá que o processo do aplicativo de backup Abra o arquivo e substitua a verificação de segurança padrão. Para restaurar o arquivo, o aplicativo de backup usaria a seguinte sintaxe de chamada de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ao abrir o arquivo a ser gravado.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Há situações em que um aplicativo de backup deve ser capaz de alterar as configurações de controle de acesso de um arquivo ou diretório. Um exemplo é quando as configurações de controle de acesso da cópia residente em disco de um arquivo ou diretório são diferentes da cópia de backup. Isso aconteceria se essas configurações fossem alteradas após o backup do arquivo ou diretório, ou se ele estava corrompido.

O sinalizador de semântica de backup de sinalizador de arquivo especificado na chamada para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fornece a permissão de processo do aplicativo de backup para ler as configurações de controle de acesso do arquivo ou diretório. **\_ \_ \_** Com essa permissão, o processo do aplicativo de backup pode chamar [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) para leitura e não redefinir as configurações de controle de acesso.

Se um aplicativo de backup precisar ter acesso às [configurações de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists)no nível do sistema, o sinalizador de **\_ \_ segurança do sistema de acesso** deverá ser especificado no valor do parâmetro *dwDesiredAccess* passado para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Os aplicativos de backup chamam [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) para ler os arquivos e diretórios especificados para a operação de restauração e [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) para escrevê-los.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
