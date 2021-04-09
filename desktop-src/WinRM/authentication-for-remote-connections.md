---
title: Autenticação para conexões remotas
description: Gerenciamento Remoto do Windows mantém a segurança para a comunicação entre computadores dando suporte a vários métodos padrão de autenticação e criptografia de mensagens.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2020
ms.locfileid: "104007251"
---
# <a name="authentication-for-remote-connections"></a>Autenticação para conexões remotas

Gerenciamento Remoto do Windows mantém a segurança para a comunicação entre computadores dando suporte a vários métodos padrão de autenticação e criptografia de mensagens.

## <a name="default-group-access"></a>Acesso de grupo padrão

Durante a instalação, o WinRM cria o grupo local **WinRMRemoteWMIUsers \_ \_**. Em seguida, o WinRM restringe o acesso remoto a qualquer usuário que não seja membro do grupo de administração local ou do grupo **WinRMRemoteWMIUsers \_ \_** . Você pode adicionar um usuário local, um usuário de domínio ou um grupo de domínio a **WinRMRemoteWMIUsers \_ \_** digitando **net local WinRMRemoteWMIUsers \_ \_ /Add <domain> \\ <username>** no prompt de comando. Opcionalmente, você pode usar o Política de Grupo para adicionar um usuário ao grupo.

## <a name="default-authentication-settings"></a>Configurações de autenticação padrão

As credenciais padrão, o nome de usuário e a senha são as credenciais para a conta de usuário conectada que executa o script.

**Para alterar para outra conta em um computador remoto**

1.  Especifique as credenciais em um objeto [**ConnectionOptions**](connectionoptions.md) ou [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) e forneça isso à chamada [**CreateSession**](wsman-createsession.md) .
2.  Defina o **WSManFlagCredUserNamePassword** no parâmetro *flags* na chamada [**CreateSession**](wsman-createsession.md) .

A lista a seguir contém uma lista do que ocorre quando um script ou aplicativo é executado sob as credenciais padrão:

-   [*Kerberos*](windows-remote-management-glossary.md) é o método padrão de autenticação quando o cliente está em um domínio e a cadeia de caracteres de destino remoto não é uma das seguintes opções: localhost, 127.0.0.1 ou \[ :: 1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) é o método padrão quando o cliente não está em um domínio, mas a cadeia de caracteres de destino remoto é uma das seguintes: localhost, 127.0.0.1 ou \[ :: 1 \] .

Se você fornecer credenciais explícitas com um objeto [**ConnectionOptions**](connectionoptions.md) , Negotiate será o método padrão. A autenticação de negociação determina se o método de autenticação em andamento é Kerberos ou NTLM, dependendo se os computadores estão em um domínio ou grupo de trabalho. Se estiver se conectando a um computador de destino remoto usando uma conta local, a conta deverá ser prefixada com o nome do computador. Por exemplo, \\ myusername.

Se você especificar Negotiate, Digest ou autenticação básica e falhar em fornecer um objeto [**ConnectionOptions**](connectionoptions.md) , receberá um erro indicando que as credenciais explícitas são necessárias. Se o HTTPS não for o transporte, o computador remoto de destino deverá ser configurado na lista de computadores host confiáveis.

Para obter mais informações sobre os tipos de autenticação que estão habilitados nas definições de configuração padrão, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Autenticação Básica

Para estabelecer explicitamente a autenticação [*básica*](windows-remote-management-glossary.md) na chamada para [**WSMan. CreateSession**](wsman-createsession.md), defina os sinalizadores **WSManFlagUseBasic** e **WSManFlagCredUserNamePassword** no parâmetro *flags* . A autenticação básica é desabilitada nas definições de configuração padrão para o cliente WinRM e o servidor WinRM.

## <a name="digest-authentication"></a>Autenticação Digest

Para estabelecer explicitamente a autenticação [*Digest*](windows-remote-management-glossary.md) na chamada para [**WSMan. CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseDigest** no parâmetro *flags* . Não há suporte para Digest. Ele não pode ser configurado para o componente do servidor WinRM.

## <a name="negotiate-authentication"></a>Negociar autenticação

Para estabelecer explicitamente a autenticação de [*negociação*](windows-remote-management-glossary.md) , também conhecida como autenticação integrada do Windows, na chamada para [**WSMan. CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseNegotiate** no parâmetro *flags* .

O [UAC (controle de conta de usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afeta o acesso ao serviço WinRM. Quando a autenticação de negociação é usada em um grupo de trabalho, somente a conta de administrador interno pode acessar o serviço. Para permitir que todas as contas no grupo administradores acessem o serviço, defina o seguinte valor de registro:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticação Kerberos

Para estabelecer explicitamente a autenticação [*Kerberos*](windows-remote-management-glossary.md) na chamada para [**WSMan. CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseKerberos** no parâmetro *flags* . Os computadores cliente e servidor devem ser ingressados em um domínio. Se você usar o Kerberos como o método de autenticação, não poderá usar um endereço IP na chamada para [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticação baseada em certificado do cliente

Para estabelecer a autenticação baseada em certificado de cliente na chamada para [**WSMan. CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseClientCertificate** no parâmetro *flags* .

Primeiro, você deve habilitar a autenticação de certificado no cliente e no serviço usando a ferramenta de linha de comando WinRM. Para obter mais informações, consulte [habilitando opções de autenticação](#enabling-or-disabling-authentication-options). Você também deve criar uma entrada na tabela CertMapping no computador do servidor WinRM. Isso estabelece um mapeamento entre um ou mais certificados e uma conta local. Depois que o certificado tiver sido usado para autenticação e autorização, a conta local correspondente será usada para operações executadas pelo serviço WinRM.

O mapeamento pode ser criado para um URI de recurso específico. Para saber mais, incluindo como criar uma entrada de tabela CertMapping, digite **winrm help CertMapping** no prompt de comando.

> [!Note]  
> O certificado de tamanho máximo utilizável pelo WinRM neste contexto é 16 KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Habilitando ou desabilitando opções de autenticação

A opção de autenticação padrão na instalação do sistema é Kerberos. Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

Se o seu script ou aplicativo exigir um método de autenticação específico que não esteja habilitado, você deverá alterar a configuração para habilitar esse tipo de autenticação. Essa alteração pode ser feita usando a ferramenta de linha de comando **WinRM** ou por meio de política de grupo para o **objeto gerenciamento remoto do Windows política de grupo**. Você também pode optar por desabilitar determinados métodos de autenticação.

**Para habilitar ou desabilitar a autenticação com a ferramenta WinRM**

1.  Para definir a configuração para o cliente WinRM, use o comando **WinRM Set** e especifique o cliente. Por exemplo, o comando a seguir desabilita a autenticação Digest para o cliente.

    **WinRM Set WinRM/config/Client/auth @ {Digest = "false"}**

2.  Para definir a configuração do servidor WinRM, use o comando **WinRM Set** e especifique o serviço. Por exemplo, o comando a seguir habilita a autenticação Kerberos para o serviço.

    **WinRM Set WinRM/config/Service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> </dl>

 

 




