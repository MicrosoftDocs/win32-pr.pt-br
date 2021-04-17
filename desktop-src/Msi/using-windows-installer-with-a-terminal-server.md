---
description: Os itens a seguir podem afetar Windows Installer instalações ao usar um servidor de terminal. Os desenvolvedores de instalação devem sempre testar se o pacote de Windows Installer é instalado conforme o esperado quando os usuários também estão usando um servidor de terminal.
ms.assetid: deda9efa-a0fc-4b4e-a531-650ac201fd84
title: Usando Windows Installer com um Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d471fa19b4588a01a2730af44fa5e9d978d18859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461044"
---
# <a name="using-windows-installer-with-a-terminal-server"></a>Usando Windows Installer com um Terminal Server

Os itens a seguir podem afetar Windows Installer instalações ao usar um servidor de terminal. Os desenvolvedores de instalação devem sempre testar se o pacote de Windows Installer é instalado conforme o esperado quando os usuários também estão usando um servidor de terminal.

-   Em sistemas operacionais anteriores ao Windows Server 2008 e ao Windows Vista, a política do sistema [EnableAdminTSRemote](enableadmintsremote.md) deve ser definida para permitir que os administradores executem instalações na sessão do cliente. A partir do Windows Server 2008 e do Windows Vista, a política EnableAdminTSRemote não tem mais efeito. Independentemente de sua configuração, os administradores e os não administradores podem executar uma instalação na sessão do cliente ou na sessão do console. Os administradores e os não administradores sempre podem executar Windows Installer instalações na sessão do console.
-   O Windows Installer impedirá a instalação no [contexto de instalação](installation-context.md) por usuário se a[política do sistema](system-policy.md) [DisableUserInstalls](disableuserinstalls.md)estiver definida como 1. Nesse caso, o instalador ignora todos os aplicativos registrados como por usuário e pesquisa apenas os aplicativos registrados como por máquina.
-   Quando um administrador executa uma instalação em uma sessão de cliente de um servidor de terminal hospedado no Windows 2000, a instalação deve usar um caminho UNC e não uma letra de unidade mapeada.

Os desenvolvedores devem aderir às diretrizes a seguir ao desenvolver um componente Windows Installer que possa ser usado com um servidor de terminal.

-   Grave todas as informações do registro **HKCU** na parte do  \\ **software** HKCU do registro.
-   Não é recomendável armazenar informações de configuração em arquivos INI.
-   Gravar informações por usuário no registro quando o aplicativo for executado pela primeira vez e não no momento da instalação. Se você precisar gravar informações por usuário no registro no momento da instalação, separe as informações por usuário e por computador em diferentes componentes de Windows Installer. Crie o pacote de modo que o instalador não tente validar e reparar os componentes que contêm informações por usuário quando o aplicativo for instalado.
-   Um pacote usado somente para instalações por máquina deve gravar variáveis de ambiente no ambiente do computador, incluindo \* na coluna nome da [tabela de ambiente](environment-table.md). Se o pacote puder ser usado para instalações por usuário ou instalações por computador, use dois componentes. Inclua o componente por usuário na tabela de [componentes](condition-table.md) e insira as configurações de usuário na tabela de ambiente. Inclua o componente por computador na tabela de componentes e insira as configurações do computador na tabela de ambiente. Controle qual componente é instalado usando instruções condicionais com base na propriedade [**AllUsers**](allusers.md) no campo condição da tabela de componentes.
-   Ao executar instalações por máquina de um servidor de terminal, o instalador grava variáveis de ambiente por usuário para **HKCU** \\ **.** \\ **Ambiente** padrão. Como o servidor de terminal não replica essa seção do registro, a instalação não define as variáveis de ambiente por usuário.
-   Como um servidor pode ser configurado para impedir que os usuários reparem aplicativos, seu aplicativo deve lidar normalmente com o caso de chaves de registro ausentes.

O seguinte se aplica quando um pacote de Windows Installer que usa DLL, EXE ou [ações personalizadas](custom-actions.md) de script é instalado no contexto de instalação por máquina em um servidor de terminal. Nesse caso, o instalador define a propriedade [**TerminalServer**](terminalserver.md) .

-   Ações personalizadas adiadas são executadas no contexto do sistema local, a menos que a ação tenha o atributo **msidbCustomActionTypeTSAware** . Isso é verdadeiro mesmo que a ação personalizada represente o usuário em um sistema que não seja um servidor de terminal. Observe que, se uma ação personalizada que tenha o atributo **msidbCustomActionTypeTSAware** alterar o registro do usuário, o instalador não garantirá automaticamente que essas alterações também sejam feitas no registro de cada usuário no computador.
-   Qualquer operação de registro em uma ação personalizada adiada que leia do hive do registro **HKCU** vê o hive do registro padrão do sistema e não o hive do registro do usuário atual.
-   Todas as operações de registro em uma ação personalizada adiada que grava no \\ **software** HKCU são detectadas pelo instalador e copiadas para cada usuário do computador no próximo logon do usuário.
-   Todas as operações de registro em uma ação personalizada adiada que gravam em **HKCU**, mas que não estão sob a  \\ chave do registro do **software** HKCU, não são detectadas pelo instalador ou copiadas.

Para obter mais informações, consulte [serviços de terminal](../termserv/terminal-services-portal.md) no SDK (Software Development Kit) do Microsoft Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[EnableAdminTSRemote](enableadmintsremote.md)
</dt> <dt>

[**Propriedade TerminalServer**](terminalserver.md)
</dt> <dt>

[**Propriedade RemoteAdminTS**](remoteadmints.md)
</dt> <dt>

[Serviços de Terminal](../termserv/terminal-services-portal.md)
</dt> </dl>

 

 
