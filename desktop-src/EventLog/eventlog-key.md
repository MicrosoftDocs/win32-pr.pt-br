---
description: 'O log de eventos contém os seguintes logs padrão, bem como os logs personalizados:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Chave do log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b60a2a935267ddeed52a82602c1192ff23d7005
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477802"
---
# <a name="eventlog-key"></a>Chave do log de eventos

O log de eventos contém os seguintes logs padrão, bem como os logs personalizados:



| Log             | Descrição                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aplicativo** | Contém eventos registrados por aplicativos. Por exemplo, um aplicativo de banco de dados pode registrar um erro de arquivo. O desenvolvedor do aplicativo decide quais eventos registrar.                                                                             |
| **Segurança**    | Contém eventos como tentativas de logon válidas e inválidas, bem como eventos relacionados ao uso de recursos, como criar, abrir ou excluir arquivos ou outros objetos. Um administrador pode iniciar a auditoria para registrar eventos no log de segurança. |
| **System**      | Contém eventos registrados por componentes do sistema, como a falha de um driver ou outro componente do sistema a ser carregado durante a inicialização.                                                                                                               |
| *CustomLog*     | Contém eventos registrados por aplicativos que criam um log personalizado. O uso de um log personalizado permite que um aplicativo controle o tamanho do log ou anexe ACLs para fins de segurança sem afetar outros aplicativos.                         |



 

O serviço de log de eventos usa as informações armazenadas na chave do registro **EventLog** . A chave **EventLog** contém várias subchaves, chamadas *logs*. Cada log contém informações que o serviço de log de eventos usa para localizar recursos quando um aplicativo grava e lê o log de eventos.

A estrutura da chave **EventLog** é a seguinte:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

Observe que os controladores de domínio registram eventos no **serviço de diretório** e nos logs do serviço de **replicação de arquivo** e nos servidores DNS registram eventos no **servidor DNS**.

Cada log pode conter os valores de registro a seguir.




| Valor do Registro | Descrição | 
|----------------|-------------|
| <strong>Imposto alfandegário</strong> | Restringe o acesso ao log de eventos. Esse valor é do tipo REG_SZ. O formato usado é SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ). Construa uma ACL que concede um ou mais dos seguintes direitos:<dl> Clear (0x0004)<br />Leitura (0x0001)<br />Gravação (0x0002)<br /></dl> Para ser um SDDL sintaticamente válido, o valor alfandegário deve especificar um proprietário e um proprietário do grupo (por exemplo, O:BAG: SY), mas o proprietário e o proprietário do grupo não são usados. Se a alfândega estiver definida como um valor incorreto, um evento será disparado no log de eventos do sistema quando o serviço de log de eventos for iniciado e o log de eventos receberá um descritor de segurança padrão que é idêntico ao valor alfandegário original do log do aplicativo. Não há suporte para SACLs.<br /> Para obter mais informações, consulte <a href="event-logging-security.md">segurança de log de eventos</a>.<br /><strong>Windows Server 2003:</strong> Há suporte para SACLs.<br /><strong>Windows XP/2000:</strong> Não há suporte para esse valor.<br /><br /> | 
| <strong>DisplayNamefile</strong> | Este valor não é usado. <strong>Windows Server 2003 e Windows XP/2000:</strong> Nome do arquivo que armazena o nome localizado do log de eventos. O nome armazenado nesse arquivo aparece como o nome do log em Visualizador de Eventos. Se essa entrada não aparecer no registro de um log de eventos, Visualizador de Eventos exibirá o nome da subchave do registro como o nome do log. Esse valor é do tipo REG_EXPAND_SZ. O valor padrão é% SystemRoot% \system32\els.dll.<br /> | 
| <strong>DisplayNameid</strong> | Este valor não é usado. <strong>Windows Server 2003 e Windows XP/2000:</strong> Número de identificação da mensagem da cadeia de caracteres do nome do log. Esse número indica a mensagem na qual o nome de exibição localizado é exibido. A mensagem é armazenada no arquivo especificado pelo valor <strong>displaynamefile</strong> . Esse valor é do tipo REG_DWORD.<br /> | 
| <strong>Arquivo</strong> | Caminho totalmente qualificado para o arquivo em que cada log de eventos é armazenado. Isso permite que Visualizador de Eventos e outros aplicativos localizem os arquivos de log. Esse valor é do tipo REG_SZ ou REG_EXPAND_SZ. Esse valor é opcional. Se o valor não for especificado, o padrão será%SystemRoot%\system32\winevt\logs\ seguido por um nome de arquivo baseado no nome da chave do registro do log de eventos. O caminho do arquivo de log de eventos específico deve ser definido usando o utilitário de linha de comando wevtutil.exe ou usando a função <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> com EvtChannelLoggingConfigLogFilePath passado para o parâmetro <em>PropertyId</em> .<br /> Se um arquivo específico for definido, certifique-se de que o serviço log de eventos tenha permissões completas no arquivo.<br /> Esse valor precisa ser um nome de arquivo válido para um arquivo localizado em um diretório local (não um computador remoto, não um dispositivo DOS, não um disquete, e não um pipe). Se a configuração do arquivo estiver errada, um evento será disparado no log de eventos do sistema quando o serviço de log de eventos for iniciado.<br /> Não use variáveis de ambiente, no caminho para o arquivo, que não pode ser expandido no contexto do serviço de log de eventos.<br /><strong>Windows Server 2003 e Windows XP/2000:</strong> O padrão desse valor é%SystemRoot%\system32\config\ seguido por um nome de arquivo baseado no nome da chave do registro do log de eventos. Se a configuração do arquivo for definida como um valor inválido, o log não será inicializado corretamente ou todas as solicitações irão para o log padrão (aplicativo).<br /> | 
| <strong>MaxSize</strong> | Tamanho máximo, em bytes, do arquivo de log. Esse valor é do tipo REG_DWORD. O valor deve ser definido como um múltiplo de 64K para um sistema, aplicativo ou log de segurança. O valor padrão é 1MB. <strong>Windows Server 2003 e Windows XP/2000:</strong> O valor é limitado a 0xFFFFFFFF, e o valor padrão é 512K.<br /> | 
| <strong>PrimaryModule</strong> | Esse valor não é usado. <strong>Windows Server 2003 e Windows XP/2000:</strong> Esse valor é o nome da subchave que contém os valores padrão para as entradas na subchave da origem do evento. Esse valor é do tipo REG_SZ.<br /> | 
| <strong>Retenção</strong> | Esse valor é do tipo REG_DWORD. O valor padrão é 0. Se esse valor for 0, os registros de eventos serão sempre substituídos. Se esse valor for 0xFFFFFFFF ou qualquer valor diferente de zero, os registros nunca serão substituídos. Quando o arquivo de log atingir seu tamanho máximo, você deverá limpar o log manualmente; caso contrário, novos eventos serão descartados. Você também deve limpar o log antes de poder alterar seu tamanho. <strong>Windows Server 2003 e Windows XP/2000:</strong> Esse valor é o intervalo de tempo, em segundos, que os registros de eventos são protegidos de serem substituídos. Quando a idade de um evento atingir ou exceder esse valor, ela poderá ser substituída.<br /> | 
| <strong>Fontes</strong> | Este valor não é usado. <strong>Windows Server 2003 e Windows XP/2000:</strong> Nomes dos aplicativos, serviços ou grupos de aplicativos que gravam eventos nesse log. Esse valor só deve ser lido e não alterado. O serviço log de eventos mantém a lista com base em cada programa listado em uma subchave no log. Esse valor é do tipo REG_MULTI_SZ.<br /> | 
| <strong>AutoBackupLogFiles</strong> | Esse valor é do tipo REG_DWORD e é usado pelo serviço log de eventos para determinar se um log de eventos deve ser salvo automaticamente. O valor padrão é 0, que desabilita o backup automático. O serviço fará o backup do arquivo de log somente se o valor de retenção for-1 (0xFFFFFFFF). Outros valores serão ignorados. <strong>Windows Server 2003:</strong> A retenção pode ser definida como-1 (0xFFFFFFFF) ou 1 (0x00000001) para que o AutoBackupLogFiles funcione. Outros valores serão ignorados.<br /> | 
| <strong>RestrictGuestAccess</strong> | Este valor não é usado. <strong>Windows XP/2000:</strong> Esse valor é do tipo REG_DWORD e o valor padrão é 1. Quando o valor é definido como 1, ele restringe o acesso de conta de convidado e anônima ao log de eventos e, quando esse valor for 0, ele permitirá acesso de conta de convidado ao log de eventos.<br /> | 
| <strong>Isolamento</strong> | Define as permissões de acesso padrão para o log. Esse valor é do tipo REG_SZ. É possível especificar um dos seguintes valores:<ul><li><strong>Aplicativo</strong></li><li><strong>System</strong></li><li><strong>Personalizado</strong></li></ul>O isolamento padrão é <strong>Application</strong>. As permissões padrão para Application <strong>são</strong> (mostradas usando SDDL): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system               (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins            (read, write, clear)            L"(A;;0x7;;;SO)"                    // server operators           (read, write, clear)            L"(A;;0x3;;;IU)"                    // INTERACTIVE LOGON          (read, write)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON             (read, write)            L"(A;;0x3;;;S-1-5-3)"               // BATCH LOGON                (read, write)            L"(A;;0x3;;;S-1-5-33)"              // write restricted service   (read, write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers          (read) </code></pre>As permissões padrão para <strong>System são</strong> (mostradas usando SDDL): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system             (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins          (read, write, clear)            L"(A;;0x3;;;BO)"                    // backup operators         (read, write)            L"(A;;0x5;;;SO)"                    // server operators         (read, clear)             L"(A;;0x1;;;IU)"                    // INTERACTIVE LOGON        (read)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON           (read, write)            L"(A;;0x1;;;S-1-5-3)"               // BATCH LOGON              (read)            L"(A;;0x2;;;S-1-5-33)"              // write restricted service (write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers        (read)</code></pre>As permissões padrão para <strong>Isolamento</strong> personalizado são as mesmas que Application.<br /><strong>Windows Server 2003 e Windows XP/2000:</strong> Esse valor não está disponível.<br /> | 




 

Cada log também contém fontes de eventos. Para obter mais informações, consulte [Fontes de eventos](event-sources.md).

