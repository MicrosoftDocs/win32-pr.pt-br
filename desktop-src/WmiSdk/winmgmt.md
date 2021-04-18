---
description: Winmgmt é o serviço WMI no processo SVCHOST em execução no &\# 0034; LocalSystem&\# 0034; conta.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814054"
---
# <a name="winmgmt"></a>winmgmt

Winmgmt é o serviço WMI dentro do processo do SVCHOST em execução na conta "LocalSystem".

Em todos os casos, o serviço WMI é iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicita conexão a um namespace WMI. Para obter mais informações, confira [Iniciar e interromper o serviço WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> O WMI é um componente fundamental do sistema operacional Windows que permite que desenvolvedores e administradores de ti gravem scripts e aplicativos para automatizar determinadas tarefas. Winmgmt.exe é o serviço que permite que o WMI seja executado em seu computador local. Para obter mais informações sobre como usar o WMI, consulte [usando o WMI](using-wmi.md). Se você recebeu uma mensagem de erro referente a winmgmt.exe, consulte [solução de problemas de WMI](wmi-troubleshooting.md). Para obter mais informações sobre Winmgmt.exe, consulte [usando as ferramentas de gerenciamento do WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Quando executado no prompt de comando, o serviço WMI tem as seguintes opções.

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>Comutadores

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup***<filename>* 
</dt> <dd>

Faz com que o WMI faça backup do repositório para o nome de arquivo especificado. O argumento *filename* deve conter o caminho completo para o local do arquivo. Esse processo requer um bloqueio de gravação no repositório para que as operações de gravação no repositório sejam suspensas até que o processo de backup seja concluído.

Se você não especificar um caminho para o arquivo, ele será colocado no diretório% windir% \\ System32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>**<flag>* 
</dt> <dd>

Restaura manualmente o repositório WMI do arquivo de backup especificado. O argumento *filename* deve conter o caminho completo para o local do arquivo de backup. Para executar a operação de restauração, o WMI salva o repositório existente para fazer write-back se a operação falhar. Em seguida, o repositório é restaurado do arquivo de backup especificado no argumento *filename* . Se o acesso exclusivo ao repositório não puder ser obtido, os clientes existentes serão desconectados do WMI.

O argumento de *sinalizador* deve ser 1 (forçar a desconexão de usuários e restauração) ou 0 (restauração padrão, se nenhum usuário estiver conectado) e especificar o modo de restauração.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<winmgmt-Service-process-id>* 
</dt> <dd>

Registra as bibliotecas de desempenho do computador com o WMI. A PID do WMI é a ID do processo do serviço WMI.

Necessário somente se as classes do monitor de desempenho não retornarem resultados confiáveis.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]
</dt> <dd>

Move o serviço Winmgmt para um processo autônomo do svchost que tem um ponto de extremidade DCOM fixo. O ponto de extremidade padrão é "ncacn \_ IP \_ TCP. 0.24158". No entanto, o ponto de extremidade pode ser alterado executando Dcomcnfg.exe. Para obter mais informações sobre como configurar uma porta fixa para o WMI, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).

O argumento de *nível* é o nível de autenticação para o processo Svchost. O WMI normalmente é executado como parte de um host de serviço compartilhado e você não pode aumentar o nível de autenticação somente para WMI. Se o *nível* não for especificado, o padrão será 4 (**RPC \_ C \_ Authn \_ nível \_ PKT** ou **WbemAuthenticationLevelPkt**).

Você pode executar o WMI com mais segurança, aumentando o nível de autenticação para privacidade de pacote (**privacidade do PCT no \_ nível de \_ autenticação RPC \_ \_ \_ C** ou **WbemAuthenticationLevelPktPrivacy**). Os níveis de autenticação para Visual Basic e script são descritos em [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Para C++, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md). Para obter mais informações, consulte [mantendo a segurança do WMI](maintaining-wmi-security.md).

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Move o serviço Winmgmt para o processo compartilhado do svchost.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository***<path>* 
</dt> <dd>

Executa uma verificação de consistência no repositório do WMI. Quando você adiciona a opção **/verifyrepository** sem o *<path>* argumento, o repositório ao vivo atualmente usado pelo WMI é verificado. Ao especificar o argumento *path* , você pode verificar qualquer cópia salva do repositório. Nesse caso, o argumento de caminho deve conter o caminho completo para a cópia de repositório salva. O repositório salvo deve ser uma cópia de toda a pasta do repositório. Para obter mais informações sobre os erros retornados por esse comando, consulte a seção comentários.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Executa uma verificação de consistência no repositório do WMI e, se uma inconsistência for detectada, recria o repositório. O conteúdo do repositório inconsistente é mesclado no repositório recriado, se ele puder ser lido. A operação Salvage sempre funciona com o repositório que o serviço WMI está usando no momento. Para obter mais informações sobre os erros retornados por esse comando, consulte a seção comentários.

% Arquivos MOF que contêm a instrução de pré-processador de [**\# recuperação automática de pragma**](pragma-autorecover.md) são restaurados no repositório.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

O repositório é redefinido para o estado inicial quando o sistema operacional é instalado pela primeira vez. Os arquivos MOF que contêm a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) são restaurados no repositório.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa ferramenta está localizada no diretório% windir% \\ System32 \\ WBEM. Para obter uma lista das opções disponíveis, digite `WinMgmt /?` no prompt de comando.

O repositório WMI, também conhecido como repositório CIM, não é apenas um único arquivo, mas uma coleção de arquivos dentro da pasta de repositório que funciona em conjunto como um banco de dados. Quando você usa a opção **/backup** para fazer backup do repositório, o backup resultante é um arquivo compactado único.

O WMI retornará o **erro de erro \_ interno do \_ BD \_** (net helpmsg 1358) se uma operação de verificação indicar que o repositório não está em um estado consistente. Esse erro pode ser retornado de qualquer comando que executa a verificação do repositório, como **/verifyrepository** ou **/salvagerepository**.

> [!Note]
>
> Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.
>
> Para obter mais informações sobre a origem do problema, baixe e execute a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo. Você pode baixar o [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Conectando-se ao WMI remotamente a partir do vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

