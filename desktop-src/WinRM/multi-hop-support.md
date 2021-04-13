---
title: Suporte a vários saltos no WinRM
description: O Gerenciamento Remoto do Windows (WinRM) dá suporte à delegação de credenciais de usuário em vários computadores remotos.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456896"
---
# <a name="multi-hop-support-in-winrm"></a>Suporte a vários saltos no WinRM

O Gerenciamento Remoto do Windows (WinRM) dá suporte à delegação de credenciais de usuário em vários computadores remotos. A funcionalidade de suporte de vários saltos agora pode usar o Credential Security Service Provider (CredSSP) para autenticação. O CredSSP permite que um aplicativo delegue as credenciais do usuário do computador cliente para o servidor de destino.

A autenticação CredSSP destina-se a ambientes em que a delegação de Kerberos não pode ser usada. O suporte para CredSSP foi adicionado para permitir que um usuário se conecte a um servidor remoto e tenha a capacidade de acessar um computador de segundo salto, como um compartilhamento de arquivos.

Para obter mais informações sobre CredSSP, consulte [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> Os clientes e servidores WinRM oferecerão suporte à autenticação CredSSP somente com credenciais explícitas.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Instalação e detalhes da configuração de suporte de salto múltiplo

Há vários mecanismos para definir as configurações do WinRM. No procedimento a seguir, o utilitário **WinRM** e o editor de política de grupo (**gpedit. msc**) são usados. O CredSSP também pode ser habilitado para o WinRM usando o Windows PowerShell. Consulte os cmdlets [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)e [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) do Windows PowerShell para obter informações de configuração detalhadas e exemplos de uso.

A delegação de CredSSP deve ser habilitada nas configurações do cliente e nas configurações do serviço no computador remoto. Além disso, o uso de CredSSP requer a configuração de um [*ouvinte*](windows-remote-management-glossary.md) http ou HTTPS no servidor.

**Para configurar o suporte a vários saltos usando a autenticação CredSSP para WinRM**

1.  O CredSSP deve ser habilitado nas definições de configuração do cliente. Esse sinalizador pode ser habilitado manualmente ou por meio de uma configuração de Política de Grupo. A configuração padrão é **False**. A política **permitir a autenticação CredSSP** está localizada no seguinte caminho: configuração do computador \\ modelo \\ administrativo componentes \\ do Windows gerenciamento remoto do Windows (WinRM) \\ WinRM Client.

    O comando a seguir demonstra como usar o utilitário WinRM para habilitar o CredSSP no cliente WinRM:

    **WinRM Set WinRM/config/Client/auth @ {CredSSP = "true"}**

2.  O CredSSP deve ser habilitado nas definições de configuração do serviço WinRM. Esse sinalizador pode ser habilitado manualmente ou por meio de uma configuração de Política de Grupo. A configuração padrão é **False**. A política **permitir a autenticação CredSSP** está localizada no seguinte caminho: configuração do computador \\ modelo \\ administrativo componentes \\ do Windows gerenciamento remoto do Windows (WinRM) \\ WinRM Service.

    O comando a seguir demonstra como usar o utilitário WinRM para habilitar o CredSSP no serviço WinRM:

    **WinRM Set WinRM/config/Service/auth @ {CredSSP = "true"}**

3.  A configuração de política permitir a delegação de credenciais atualizadas (**AllowFreshCredentials**) deve ser habilitada no cliente WinRM e um SPN (nome da entidade de serviço) com o prefixo WSMan deve ser adicionado à política. O SPN representa o computador de destino ao qual as credenciais do usuário podem ser delegadas. O SPN pode ser definido como um ou mais computadores. A tabela a seguir contém exemplos de formatos válidos para SPNs.

    

    | SPN                                       | Descrição                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/MyComputer. mydomain. com<br/>  | Servidor WinRM em execução em myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* . mydomain.com<br/>          | Todos os servidores WinRM em execução no myDomain.com.<br/>                               |
    | WSMAN/ \* . fabrikam.mydomain.com<br/> | Todos os servidores WinRM em execução no em todos os computadores em. fabrikam.myDomain.com.<br/> |

    

     

    Para obter mais informações sobre como definir políticas de grupo, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

    Para obter mais informações sobre a política **AllowFreshCredentials** , consulte a descrição da política fornecida pelo editor de política de grupo e [KB 951608](https://support.microsoft.com/kb/951608). A política **AllowFreshCredentials** está localizada no seguinte caminho: configuração do computador \\ modelos administrativos \\ delegação de credenciais do sistema \\ .

4.  Um [*ouvinte*](windows-remote-management-glossary.md) HTTPS ou http deve ser configurado no servidor. A impressão digital do certificado usada para configurar o *ouvinte* HTTPS também é usada para definir a configuração CertificateThumbprint nas configurações do serviço WinRM.

    O comando a seguir demonstra como usar o utilitário WinRM para configurar um [*ouvinte*](windows-remote-management-glossary.md)https:

    **winrm quickconfig-Transport: https**

Se a autenticação Kerberos entre o cliente e o servidor não for possível, o usuário deverá configurar uma das seguintes configurações para suporte a vários saltos:

-   Para maior segurança, o usuário deve adicionar o atributo **CertificateThumbprint** à configuração do serviço WinRM. Se o serviço WinRM estiver configurado com um atributo **CertificateThumbprint** , o serviço tentará localizar o certificado correspondente no repositório do computador local e usará esse certificado para a autenticação CredSSP. Se o serviço WinRM usar um certificado do repositório do computador local para autenticar o servidor, a conta de serviço de rede deverá ter permissão de acesso à chave privada do certificado.

    > [!Note]  
    > Se a configuração do serviço não estiver configurada, o servidor WinRM usará um certificado autoassinado que é criado na memória para criptografar as mensagens enviadas ao cliente. No entanto, esse certificado não é usado para autenticação.

     

-   Se nenhuma autenticação Kerberos nem impressão digital de certificado estiver disponível, o usuário poderá habilitar a autenticação NTLM. Se a autenticação NTLM for usada, a política permitir novas credenciais com **AllowFreshCredentialsWhenNTLMOnly**(autenticação de servidor somente NTML) deverá ser habilitada e um SPN com o prefixo WSMan deverá ser adicionado à política. Essa configuração é menos segura do que a autenticação Kerberos e as impressões digitais do certificado, pois as credenciais são enviadas a um servidor não autenticado.

    Para obter mais informações sobre a política **AllowFreshCredentialsWhenNTLMOnly** , consulte a descrição da política fornecida pelo editor de política de grupo e [KB 951608](https://support.microsoft.com/kb/951608). A política **AllowFreshCredentialsWhenNTLMOnly** está localizada no seguinte caminho: configuração do computador \\ modelos administrativos \\ delegação de credenciais do sistema \\ .

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Usando a autenticação CredSSP com credenciais explícitas

Um usuário pode especificar credenciais explícitas em HTTP e HTTPS. O comando a seguir demonstra como usar o utilitário WinRM para executar uma operação remota usando a autenticação CredSSP com credenciais explícitas por HTTPS:

**OPERAÇÃO do WinRM-remota: https://myMachine -autenticação: CredSSP-username: myusername-senha: mypassword**

 

