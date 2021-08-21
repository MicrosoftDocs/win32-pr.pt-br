---
description: ao executar um backup ou restauração do VSS, o estado do sistema Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos. Esses elementos devem ser sempre tratados como uma unidade por operações de backup e restauração.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Fazendo backup e restaurando o estado do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b027fa0d1a01f3d4f735494d34d4f2da2d07a0e0d82ecfd189f7a9c7c8537c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056394"
---
# <a name="backing-up-and-restoring-system-state"></a>Fazendo backup e restaurando o estado do sistema

> [!Note]  
> este tópico aplica-se ao Windows Vista, Windows Server 2008 e posterior. para obter informações sobre o Windows Server 2003, consulte [fazendo backup e restaurando o estado do sistema no Windows server 2003 R2 e no Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)

 

ao executar um backup ou restauração do VSS, o estado do sistema Windows é definido como sendo uma coleção de vários elementos principais do sistema operacional e seus arquivos. Esses elementos devem ser sempre tratados como uma unidade por operações de backup e restauração.

> [!Note]  
> a Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online em Windows (todas as versões).

 

Durante o backup e a recuperação do estado do sistema, a estratégia recomendada é fazer backup e recuperar os volumes do sistema e de inicialização, além dos arquivos enumerados pelos gravadores do estado do sistema. Os gravadores de estado do sistema são gravadores que têm o atributo de [**\_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) definido como VSS \_ UT \_ BOOTABLESYSTEMSTATE ou VSS \_ UT \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Se um gravador VSS for identificado por seu [**\_ \_ tipo de uso do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) como um gravador de estado do sistema, ele deverá ser incluído em um backup de estado do sistema, mesmo se ele for selecionável.

 

Além do sistema operacional enumerado e dos arquivos binários de driver que são enumerados pelos gravadores de estado do sistema, há alguns outros arquivos que devem ser submetidos a backup como parte do estado do sistema.

Todos os componentes relatados por um gravador de estado do sistema VSS fazem parte do estado do sistema, exceto aqueles para os quais o sinalizador de estado do sistema do CF do VSS \_ \_ não \_ \_ está definido.

Os programas de backup também devem definir a chave do registro **LastRestoreId** . Para obter mais informações, consulte [chaves e valores do registro para backup e restauração](../backup/registry-keys-for-backup-and-restore.md).

> [!Note]  
> no Windows Vista, Windows Server 2008 e posterior, os nomes e locais de alguns arquivos do sistema foram alterados da seguinte maneira.

 

## <a name="system-state"></a>Estado do Sistema

para Windows Server 2012 e posterior, além dos arquivos relatados pelos vários gravadores do estado do sistema VSS, somente os seguintes arquivos de licenciamento precisam ser incluídos explicitamente, e os seguintes arquivos DRM precisam ser excluídos explicitamente.

## <a name="windows-media-digital-rights-management-files"></a>Windows Arquivos de Rights Management digital de mídia

no Windows Server 2008 e posterior, os seguintes arquivos, incluindo todos os subdiretórios no caminho a seguir, são excluídos do estado do sistema e não devem ser submetidos a backup:

-   % ProgramData% \\ Microsoft \\ Windows \\ DRM\\

isso substitui as informações na seção Rights Management Digital Windows Media de [trabalhar com recursos de segurança e sistema de arquivos](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>Arquivos de configuração do contador de desempenho

Os arquivos de configuração do contador de desempenho estão localizados no diretório% SystemRoot% \\ System32 \\ e têm os seguintes nomes:

<dl> Perf? 00?. DATs  
??. Perfc0 DATs  
??. Perfd0 DATs  
??. Perfh0 DATs  
??. Perfi0 DATs  
???. Prfc0 DATs  
???. Prfd0 DATs  
???. Prfh0 DATs  
???. Prfi0 DATs  
</dl>

Esses arquivos são modificados apenas durante a instalação do aplicativo e devem ser armazenados em backup e restaurados durante as restaurações e backups de estado do sistema.

## <a name="iis-configuration-files"></a>Arquivos de configuração do IIS

> [!Note]  
> no Windows Vista com Service Pack 1 (SP1) e posterior, você não deve fazer backup desses arquivos. Em vez disso, use o gravador de configuração do IIS in-box. Para obter mais informações sobre esse gravador, consulte [gravadores VSS in-box](in-box-vss-writers.md).

 

Os arquivos de configuração relevantes do IIS e seus locais são listados abaixo:

-   O arquivo de machine.config do .NET FX está localizado no diretório da versão do Framework.
-   o arquivo de web.config raiz ASP.NET está localizado no diretório da versão do framework.
    > [!Note]  
    > os arquivos de configuração para o .net FX e o ASP.NET estão no diretório da versão do framework. Se várias versões do Framework estiverem instaladas no computador, esse diretório conterá um arquivo de configuração para cada versão instalada.

     

-   O arquivo de configuração central do IIS applicationHost.config está localizado no diretório% windir% \\ System32 \\ inetsrv \\ config. Para que o servidor entenda esse arquivo de configuração, há arquivos de esquema que determinam sua gramática e estrutura. Esses arquivos estão localizados no diretório de esquema de configuração% windir% \\ System32 \\ inetsrv \\ \\ .

O caminho do diretório da versão do Framework é armazenado na seguinte chave do registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ . NETFramework \\ InstallRoot**

Além disso, deve ser feito o backup das seguintes chaves de criptografia:<dl> % ProgramData% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\*  
% SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>Arquivos do Framework

É necessário fazer backup de todas as versões do .NET Framework. Os arquivos estão localizados em um ou nos dois diretórios a seguir:

<dl> % WINDIR% \\ Microsoft.NET \\ Framework  
% WINDIR% \\ Microsoft.NET \\ Framework64  
</dl>

Além disso, o backup dos arquivos de assembly deve ser feito. Esses arquivos estão localizados no seguinte diretório:<dl> assembly% windir% \\  
</dl>

## <a name="task-scheduler-task-files"></a>Agendador de Tarefas arquivos de tarefa

É necessário fazer backup dos arquivos de tarefa do Agendador de tarefas. Os arquivos estão localizados em um ou nos dois locais a seguir:

<dl> tarefas% windir% \\ System32 \\ e quaisquer subdiretórios (recursivamente)  
tarefas de% windir% \\ (sem subdiretórios)  
</dl>

 

 
