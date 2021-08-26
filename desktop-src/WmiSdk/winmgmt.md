---
description: Winmgmt é o serviço WMI dentro do processo SVCHOST em execução no &\# 0034; LocalSystem&\# 0034; conta.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: Winmgmt
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
ms.openlocfilehash: d28d37faf454accd91281034d0aeb8df5e10dddb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879871"
---
# <a name="winmgmt"></a>Winmgmt

Winmgmt é o serviço WMI dentro do processo SVCHOST em execução na conta "LocalSystem".

Em todos os casos, o serviço WMI é iniciado automaticamente quando o primeiro aplicativo de gerenciamento ou script solicita conexão com um namespace WMI. Para obter mais informações, confira [Iniciar e interromper o serviço WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> O WMI é um componente principal do sistema operacional Windows que permite que desenvolvedores e administradores de IT escrevam scripts e aplicativos para automatizar determinadas tarefas. Winmgmt.exe é o serviço que permite que o WMI seja executado no computador local. Para obter mais informações sobre como usar o WMI, [consulte Using WMI](using-wmi.md). Se você recebeu uma mensagem de erro sobre winmgmt.exe, consulte Solução de problemas [do WMI.](wmi-troubleshooting.md) Para obter mais informações sobre Winmgmt.exe, consulte [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

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

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/backup** *&lt; filename &gt;* 
</dt> <dd>

Faz com que o WMI fazer o back-up do repositório para o nome de arquivo especificado. O *argumento filename* deve conter o caminho completo para o local do arquivo. Esse processo requer um bloqueio de gravação no repositório para que as operações de gravação no repositório sejam suspensas até que o processo de backup seja concluído.

Se você não especificar um caminho para o arquivo, ele será colocado no diretório %Windir% \\ System32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *&lt; filename &gt;* *&lt; flag &gt;* 
</dt> <dd>

Restaura manualmente o repositório WMI do arquivo de backup especificado. O *argumento filename* deve conter o caminho completo para o local do arquivo de backup. Para executar a operação de restauração, o WMI salva o repositório existente para gravar novamente se a operação falhar. Em seguida, o repositório é restaurado do arquivo de backup especificado no argumento *filename.* Se o acesso exclusivo ao repositório não puder ser obtido, os clientes existentes serão desconectados do WMI.

O *argumento de* sinalizador deve ser um 1 (forçar a desconexão de usuários e a restauração) ou 0 (restauração padrão se nenhum usuário estiver conectado) e especificar o modo de restauração.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *&lt; winmgmt-service-process-id &gt;* 
</dt> <dd>

Registra as bibliotecas de desempenho do computador com o WMI. O PID do WMI é a ID do processo para o serviço WMI.

Só será necessário se as classes do monitor de desempenho não retornarem resultados confiáveis.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[ *&lt; nível &gt;*\]
</dt> <dd>

Move o serviço Winmgmt para um processo Svchost autônomo que tem um ponto de extremidade DCOM fixo. O ponto de extremidade padrão é "ncacn \_ ip \_ tcp.0.24158". No entanto, o ponto de extremidade pode ser alterado executando Dcomcnfg.exe. Para obter mais informações sobre como configurar uma porta fixa para WMI, consulte [Configurando uma porta fixa para WMI](setting-up-a-fixed-port-for-wmi.md).

O *argumento level* é o nível de autenticação para o processo Svchost. Normalmente, o WMI é executado como parte de um host de serviço compartilhado e você não pode aumentar o nível de autenticação apenas para o WMI. Se *level* não for especificado, o padrão será 4 (**RPC C \_ \_ AUTHN \_ LEVEL \_ PKT** ou **WbemAuthenticationLevelPkt**).

Você pode executar o WMI com mais segurança aumentando o nível de autenticação para Privacidade do Pacote (**RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** ou **WbemAuthenticationLevelPktPrivacy**). Os níveis de autenticação para Visual Basic e script são descritos em [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Para C++, consulte [Definindo o nível de segurança do processo padrão usando C++.](setting-the-default-process-security-level-using-c-.md) Para obter mais informações, consulte [Mantendo a segurança WMI.](maintaining-wmi-security.md)

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Move o serviço Winmgmt para o processo Svchost compartilhado.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository** *&lt; path &gt;* 
</dt> <dd>

Executa uma verificação de consistência no repositório WMI. Quando você adiciona a **opção /verifyrepository** sem o argumento *&lt; path, &gt;* o repositório ao vivo usado atualmente pelo WMI é verificado. Ao especificar o argumento *path,* você pode verificar qualquer cópia salva do repositório. Nesse caso, o argumento path deve conter o caminho completo para a cópia do repositório salvo. O repositório salvo deve ser uma cópia de toda a pasta do repositório. Para obter mais informações sobre erros retornados por este comando, consulte a seção Comentários.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Executa uma verificação de consistência no repositório WMI e, se uma inconsistência for detectada, o recriará o repositório. O conteúdo do repositório inconsistente será mesclado no repositório re-reconstruído, se puder ser lido. A operação de salvamento sempre funciona com o repositório que o serviço WMI está usando no momento. Para obter mais informações sobre erros retornados por este comando, consulte a seção Comentários.

% de arquivos MOF que contêm a instrução de pré-processador de recuperação automática [**\# pragma**](pragma-autorecover.md) são restaurados para o repositório.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

O repositório é redefinido para o estado inicial quando o sistema operacional é instalado pela primeira vez. Os arquivos MOF que contêm a instrução de pré-processador de recuperação automática [**\# pragma**](pragma-autorecover.md) são restaurados para o repositório.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa ferramenta está localizada no diretório wbem %Windir% \\ \\ System32. Para uma lista das opções disponíveis, digite `WinMgmt /?` no prompt de comando.

O repositório WMI, também conhecido como repositório CIM, não é apenas um único arquivo, mas uma coleção de arquivos dentro da pasta Repositório que funcionam juntos como um banco de dados. Quando você usa a **opção /backup** para fazer backup do repositório, o backup resultante é um único arquivo compactado.

O WMI retornará o erro **ERROR \_ INTERNAL DB \_ \_ CORRUPTION** (net helpmsg 1358) se uma operação de verificação indicar que o repositório não está em um estado consistente. Esse erro pode ser retornado de qualquer comando que executa a verificação do repositório, como **/verifyrepository** ou **/repositoryrepository**.

> [!Note]
>
> Se o WMI retornar mensagens de erro, esteja ciente de que elas podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstâncias, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.
>
> Para obter mais informações sobre a origem do problema, baixe e execute a [Utilitário de Diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de linha de comando de diagnóstico. Essa ferramenta produz um relatório que geralmente pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft a ajudá-lo. Você pode baixar o [Utilitário de Diagnóstico WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Solução de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Conectando-se ao WMI remotamente começando com o Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

