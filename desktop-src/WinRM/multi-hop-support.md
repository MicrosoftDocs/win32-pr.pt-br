---
title: Suporte a vários saltos no WinRM
description: Windows O WinRM (Gerenciamento Remoto) dá suporte à delegação de credenciais de usuário em vários computadores remotos.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76be3054fc9c0d624c206cf5a26d7788e763dfc81f1b2069f6abff8736be2388
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121756"
---
# <a name="multi-hop-support-in-winrm"></a>Suporte a vários saltos no WinRM

Windows O WinRM (Gerenciamento Remoto) dá suporte à delegação de credenciais de usuário em vários computadores remotos. A funcionalidade de suporte de vários saltos agora pode usar o CredSSP (Provedor de Serviços de Segurança de Credencial) para autenticação. O CredSSP permite que um aplicativo delegar as credenciais do usuário do computador cliente para o servidor de destino.

A autenticação CredSSP destina-se a ambientes em que a delegação Kerberos não pode ser usada. O suporte para CredSSP foi adicionado para permitir que um usuário se conecte a um servidor remoto e tenha a capacidade de acessar um computador de segundo salto, como um compartilhamento de arquivos.

Para obter mais informações sobre CredSSP, consulte [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> Os clientes e servidores WinRM darão suporte à autenticação CredSSP somente com credenciais explícitas.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Configuração e detalhes de configuração de suporte de vários saltos

Há vários mecanismos para definir as configurações do WinRM. No procedimento a seguir, o **utilitário winrm** e o editor Política de Grupo (**GPEdit.msc**) são usados. O CredSSP também pode ser habilitado para WinRM usando Windows PowerShell. Consulte os cmdlets [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [Get-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)e [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) Windows PowerShell para obter informações detalhadas de configuração e exemplos de uso.

A delegação credSSP deve ser habilitada nas configurações do cliente e nas configurações de serviço no computador remoto. Além disso, o uso do CredSSP requer a configuração de um ouvinte HTTP ou [*HTTPS*](windows-remote-management-glossary.md) no servidor.

**Para configurar o suporte de vários saltos usando a autenticação CredSSP para WinRM**

1.  CredSSP deve ser habilitado nas definições de configuração do cliente. Esse sinalizador pode ser habilitado manualmente ou por meio de uma Política de Grupo configuração. A configuração padrão é **False**. A política de autenticação **Permitir CredSSP** está localizada no seguinte caminho: Modelo Administrativo de Configuração do Computador Windows \\ \\ Componentes \\ Windows \\ WinRM (Gerenciamento Remoto).

    O comando a seguir demonstra como usar o utilitário winrm para habilitar o CredSSP no cliente WinRM:

    **winrm set winrm/config/client/auth @{CredSSP="true"}**

2.  O CredSSP deve ser habilitado nas definições de configuração do serviço WinRM. Esse sinalizador pode ser habilitado manualmente ou por meio de uma Política de Grupo configuração. A configuração padrão é **False**. A política de autenticação **Permitir CredSSP** está localizada no seguinte caminho: Modelo Administrativo de Configuração do Computador Windows \\ \\ Componentes \\ Windows \\ WinRM (Gerenciamento Remoto).

    O comando a seguir demonstra como usar o utilitário winrm para habilitar o CredSSP no serviço WinRM:

    **winrm set winrm/config/service/auth @{CredSSP="true"}**

3.  A configuração de política Permitir Delegação de Credenciais Novas (**AllowFreshCredentials**) deve ser habilitada no cliente WinRM e um SPN (Nome da Entidade de Serviço) com o prefixo WSMAN deve ser adicionado à política. O SPN representa o computador de destino ao qual as credenciais do usuário podem ser delegadas. O SPN pode ser definido como um ou mais computadores. A tabela a seguir contém exemplos de formatos válidos para SPNs.

    

    | SPN                                       | Descrição                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer.myDomain.com<br/>  | Servidor WinRM em execução myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* .myDomain.com<br/>          | Todos os servidores WinRM em execução myDomain.com.<br/>                               |
    | WSMAN/ \* .fabrikam.myDomain.com<br/> | Todos os servidores WinRM em execução no em todos os computadores no .fabrikam.myDomain.com.<br/> |

    

     

    Para obter mais informações sobre como definir Políticas de Grupo, consulte [Instalação e configuração Windows Gerenciamento Remoto.](installation-and-configuration-for-windows-remote-management.md)

    Para obter mais informações sobre **a política AllowFreshCredentials,** consulte a descrição da política fornecida pelo editor Política de Grupo e [KB 951608](https://support.microsoft.com/kb/951608). A **política AllowFreshCredentials** está localizada no seguinte caminho: Configuração do Computador Modelos Administrativos \\ \\ \\ Delegação de Credenciais do Sistema.

4.  Um ouvinte HTTPS [*ou*](windows-remote-management-glossary.md) HTTP deve ser configurado no servidor. A impressão digital do certificado usada para configurar o ouvinte *HTTPS* também é usada para definir a configuração CertificateThumbprint nas configurações do serviço WinRM.

    O comando a seguir demonstra como usar o utilitário winrm para configurar um ouvinte [*HTTPS*](windows-remote-management-glossary.md):

    **winrm quickconfig -transport:https**

Se a autenticação Kerberos entre o cliente e o servidor não for possível, o usuário deverá definir uma das seguintes configurações para suporte a vários saltos:

-   Para maior segurança, o usuário deve adicionar o atributo **CertificateThumbprint** à configuração do serviço WinRM. Se o serviço WinRM estiver configurado com um atributo **CertificateThumbprint,** o serviço tentará localizar o certificado correspondente no armazenamento do Computador Local e usará esse certificado para a autenticação CredSSP. Se o serviço WinRM usar um certificado do armazenamento de Máquinas Locais para autenticar o servidor, a conta de Serviço de Rede deverá ter permissão para acessar a chave privada do certificado.

    > [!Note]  
    > Se a configuração de serviço não estiver configurada, o servidor WinRM usará um certificado auto-assinado criado na memória para criptografar mensagens enviadas ao cliente. No entanto, esse certificado não é usado para autenticação.

     

-   Se a autenticação Kerberos nem as impressões digitais do certificado não estão disponíveis, o usuário pode habilitar a autenticação NTLM. Se a autenticação NTLM for usada, a política Permitir Novas Credenciais com Autenticação de Servidor somente NTLM (**AllowFreshCredentialsWhenNTLMOnly**) deverá ser habilitada e um SPN com o prefixo WSMAN deverá ser adicionado à política. Essa configuração é menos segura do que a autenticação Kerberos e as impressões digitais do certificado, porque as credenciais são enviadas para um servidor não autenticado.

    Para obter mais informações sobre a **política AllowFreshCredentialsWhenNTLMOnly,** consulte a descrição da política fornecida pelo editor do Política de Grupo e [KB 951608](https://support.microsoft.com/kb/951608). A **política AllowFreshCredentialsWhenNTLMOnly** está localizada no seguinte caminho: Configuração do Computador Modelos Administrativos Delegação \\ de Credenciais do \\ \\ Sistema.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Usando a autenticação CredSSP com credenciais explícitas

Um usuário pode especificar credenciais explícitas sobre HTTP e HTTPS. O comando a seguir demonstra como usar o utilitário winrm para executar uma operação remota usando a autenticação CredSSP com credenciais explícitas por HTTPS:

**winrm OPERATION -remote: https://myMachine -authentication:CredSSP -username:myUsername -password:myPassword**

 

