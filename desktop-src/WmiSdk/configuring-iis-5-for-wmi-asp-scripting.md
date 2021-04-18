---
description: Todas as configurações de autenticação são feitas por meio do Gerenciador de Serviços de Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configurando o IIS 5,0 e posterior para o script WMI ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788755"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Configurando o IIS 5,0 e posterior para o script WMI ASP

Todas as configurações de autenticação são feitas por meio do Gerenciador de Serviços de Internet.

Ao configurar o IIS (servidor de informações da Internet) 5,0 e a segurança do IIS 6,0 para scripts ASP WMI, considere os seguintes problemas:

-   [Nível de autenticação](#authentication-level)

    Você pode configurar no nível do servidor, diretório ou arquivo.

-   [Configuração de autenticação](#authentication-setting)

    Você pode definir a autenticação para o Windows anônimo, integrado ou ambos.

-   [Proteção](#protection)

    Você pode definir o ASP para executar em processo (baixa proteção) ou fora do processo usando Dllhost.exe (proteção média ou alta).

## <a name="authentication-level"></a>Nível de autenticação

Para aumentar a segurança, você pode configurar a autenticação no nível do diretório ou do arquivo.

Se a autenticação estiver definida no nível do servidor, todos os diretórios e arquivos subsequentes aderirão à autenticação do servidor, a menos que sejam explicitamente alterados no nível do diretório ou do arquivo. Você pode criar uma estrutura de diretório para conter todos os scripts WMI ASP em que as páginas HTML e ASPs específicas ao WMI podem ser configuradas independentemente do restante do servidor. Execute o procedimento a seguir para alterar o nível de autenticação de um servidor, diretório ou arquivo.

**Para definir a autenticação em qualquer nível**

1.  No painel de controle, clique duas vezes em **Ferramentas administrativas** e, em seguida, clique duas vezes no snap-in do IIS.

2.  Localize o ícone da página ASP e, em seguida, abra as propriedades do nível a ser definido, que pode ser servidor, diretório ou arquivo.

    > [!Note]  
    > Configurações de autenticação estão localizadas na guia Segurança de **diretório** ou **segurança de arquivo** da folha de **Propriedades**.

     

## <a name="authentication-setting"></a>Configuração de autenticação

Para scripts ASP WMI, a combinação de autenticação anônima desativada (desmarcada) e a autenticação integrada do Windows ativada (marcada) fornece uma oportunidade maior para definir a segurança. Para usar as configurações de autenticação do NT LAN Manager (NTLM), Passport ou Digest do IIS, você deve ativar os privilégios de habilitação remota, pois o usuário é tratado como uma identidade de rede e registrado remotamente. A configuração habilitação remota não é necessária para a autenticação anônima e básica. No entanto, o sistema é muito menos seguro quando você está usando a autenticação anônima e básica.

Se a autenticação anônima for usada com ou sem a autenticação integrada do Windows, a abordagem mais segura será usar um logon que exija que um usuário insira um nome de usuários e uma senha. O logon padrão é a identidade do IIS, mas um logon pode ser criado usando permissões específicas adequadas para os scripts ASP WMI que podem ser usados como a conta para as conexões anônimas ou convidadas.

Se você escolher um identificador de logon que não seja uma identidade do IIS, desmarque a caixa de seleção **permitir que o IIS controle a senha** e insira a senha correta. Isso força todas as conexões anônimas ou convidadas a usar o identificador de logon. Ao criar um logon separado da identidade do IIS, os privilégios de uma conta que acessa o WMI podem ser controlados sem afetar os outros diretórios ou arquivos no servidor IIS, a menos que a autenticação esteja definida no nível do servidor.

Execute o procedimento a seguir para definir os requisitos de autenticação para a página ASP usando o snap-in do IIS no painel de controle.

**Para acessar a configuração da conta**

1.  No painel de controle, clique duas vezes no ícone **Ferramentas administrativas** , abra o snap-in do IIS, localize a página ASP e abra as propriedades do nível a ser definido, que pode ser servidor, diretório ou arquivo.

    As configurações de autenticação podem ser encontradas na guia Segurança de **diretório** ou **segurança de arquivo** da folha **Propriedades** .

2.  Na área autenticação anônima, clique em **Editar**.

3.  Se um identificador de logon diferente da identidade do IIS for selecionado, desmarque a caixa de seleção **permitir que o IIS controle a senha** e insira a senha correta. Isso força todas as conexões anônimas ou convidadas a usar o identificador de logon.

Usando um logon diferente da identidade do IIS, os privilégios da conta que acessa o WMI podem ser controlados sem afetar os outros diretórios ou arquivos no servidor IIS, a menos que a autenticação esteja definida no nível do servidor.

A configuração anterior permite que o servidor IIS use a autenticação anônima em algumas áreas e uma autenticação integrada do Windows ou mista em outras.

## <a name="protection"></a>Proteção

A última consideração ao configurar o servidor IIS é a proteção a ser usada ao executar um ASP.

Você pode definir um ASP para executar o seguinte:

-   Em processo para o IIS (baixa proteção).

-   Externo ao IIS com Dllhost.exe como em pool ou fora de processo (proteção de mídia em pool).

-   Auto-host fora do processo (alta proteção).

> [!Note]  
> Para obter o melhor equilíbrio de segurança e desempenho, use o host em pool.

 

 

 



