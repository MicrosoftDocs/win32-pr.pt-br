---
title: Autenticação para conexões remotas
description: Windows O Gerenciamento Remoto mantém a segurança para comunicação entre computadores, dando suporte a vários métodos padrão de autenticação e criptografia de mensagens.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0622f3d80e923f7d910740c71ee99f0e9a0bc446cea259b292e2d645e3b5a973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858867"
---
# <a name="authentication-for-remote-connections"></a>Autenticação para conexões remotas

Windows O Gerenciamento Remoto mantém a segurança para comunicação entre computadores, dando suporte a vários métodos padrão de autenticação e criptografia de mensagens.

## <a name="default-group-access"></a>Acesso de grupo padrão

Durante a instalação, o WinRM cria o grupo local **\_ \_ WinRMRemoteWMIUsers.** Em seguida, o WinRM restringe o acesso remoto a qualquer usuário que não seja membro do grupo de administração local ou do **grupo \_ \_ WinRMRemoteWMIUsers.** Você pode adicionar um usuário local, usuário de domínio ou grupo de domínio ao **\_ \_ WinRMRemoteWMIUsers** digitando **net localgroup WinRMRemoteWMIUsers \_ \_ /add <domain> \\ <username>** no prompt de comando. Opcionalmente, você pode usar o Política de Grupo para adicionar um usuário ao grupo.

## <a name="default-authentication-settings"></a>Autenticação padrão Configurações

As credenciais padrão, o nome de usuário e a senha são as credenciais da conta de usuário conectado que executa o script.

**Para alterar para outra conta em um computador remoto**

1.  Especifique as credenciais em [**um objeto ConnectionOptions**](connectionoptions.md) [**ou IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) e as fornecerá à [**chamada CreateSession.**](wsman-createsession.md)
2.  Defina **WSManFlagCredUserNamePassword** no parâmetro *flags* na [**chamada CreateSession.**](wsman-createsession.md)

A lista a seguir contém uma lista do que ocorre quando um script ou aplicativo é executado com as credenciais padrão:

-   [*Kerberos*](windows-remote-management-glossary.md) é o método padrão de autenticação quando o cliente está em um domínio e a cadeia de caracteres de destino remoto não é uma das seguintes: localhost, 127.0.0.1 ou \[ ::1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) é o método padrão quando o cliente não está em um domínio, mas a cadeia de caracteres de destino remoto é uma das seguintes: localhost, 127.0.0.1 ou \[ ::1 \] .

Se você fornecer credenciais explícitas com um [**objeto ConnectionOptions,**](connectionoptions.md) Negotiate será o método padrão. A autenticação Negotiate determina se o método de autenticação em andamento é Kerberos ou NTLM, dependendo se os computadores estão em um domínio ou grupo de trabalho. Se estiver se conectando a um computador de destino remoto usando uma conta local, a conta deverá ser prefixada com o nome do computador. Por exemplo, myComputer \\ myUsername.

Se você especificar a autenticação Negotiate, Digest ou Basic e não fornecer um objeto [**ConnectionOptions,**](connectionoptions.md) receberá um erro indicando que são necessárias credenciais explícitas. Se HTTPS não for o transporte, o computador remoto de destino deverá ser configurado na lista de computadores host confiáveis.

Para obter mais informações sobre os tipos de autenticação habilitados nas definições de configuração padrão, consulte Instalação e configuração para [Windows Gerenciamento Remoto.](installation-and-configuration-for-windows-remote-management.md)

## <a name="basic-authentication"></a>Autenticação Básica

Para estabelecer explicitamente a autenticação [*Básica*](windows-remote-management-glossary.md) na chamada para [**WSMan.CreateSession**](wsman-createsession.md), defina os sinalizadores **WSManFlagUseBasic** e **WSManFlagCredUserNamePassword** no parâmetro *flags.* A autenticação básica está desabilitada nas definições de configuração padrão para o cliente WinRM e o servidor WinRM.

## <a name="digest-authentication"></a>Autenticação Digest

Para estabelecer explicitamente a autenticação [*Digest*](windows-remote-management-glossary.md) na chamada para [**WSMan.CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseDigest** no parâmetro *flags.* Não há suporte para Digest. Ele não pode ser configurado para o componente do servidor WinRM.

## <a name="negotiate-authentication"></a>Negociar autenticação

Para estabelecer explicitamente a autenticação [*Negotiate,*](windows-remote-management-glossary.md) também conhecida como Autenticação Integrada do Windows, na chamada para [**WSMan.CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseNegotiate** no parâmetro *flags.*

[O UAC (Controle de Conta de Usuário)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afeta o acesso ao serviço WinRM. Quando a autenticação Negotiate é usada em um grupo de trabalho, somente a conta de Administrador interno pode acessar o serviço. Para permitir que todas as contas no grupo Administradores acessem o serviço, de definido o seguinte valor do Registro:

**HKEY \_ SOFTWARE \_ DO COMPUTADOR LOCAL** Microsoft Windows Sistema de Políticas Do \\  \\  \\  \\ **CurrentVersion** \\  \\  \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Autenticação Kerberos

Para estabelecer explicitamente a autenticação [*Kerberos*](windows-remote-management-glossary.md) na chamada para [**WSMan.CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseKerberos** no parâmetro *flags.* Os computadores cliente e servidor devem ser ingressados em um domínio. Se você usar Kerberos como o método de autenticação, não poderá usar um endereço IP na chamada para [**WSMan.CreateSession**](wsman-createsession.md) ou [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Autenticação baseada em certificado do cliente

Para estabelecer a autenticação baseada em certificado do cliente na chamada para [**WSMan.CreateSession**](wsman-createsession.md), defina o sinalizador **WSManFlagUseClientCertificate** no parâmetro *flags.*

Primeiro, você deve habilitar a autenticação de certificado no cliente e no serviço usando a ferramenta de linha de comando winrm. Para obter mais informações, consulte [Habilitando opções de autenticação](#enabling-or-disabling-authentication-options). Você também deve criar uma entrada na tabela CertMapping no computador do servidor WinRM. Isso estabelece um mapeamento entre um ou mais certificados e uma conta local. Depois que o certificado tiver sido usado para autenticação e autorização, a conta local correspondente será usada para operações executadas pelo serviço WinRM.

O mapeamento pode ser criado para um URI de recurso específico. Para saber mais, incluindo como criar uma entrada de tabela CertMapping, digite **winrm help certmapping** no prompt de comando.

> [!Note]  
> O certificado de tamanho máximo acessível pelo WinRM nesse contexto é de 16KB.

 

## <a name="enabling-or-disabling-authentication-options"></a>Habilitando ou desabilitando opções de autenticação

A opção de autenticação padrão na instalação do sistema é Kerberos. Para obter mais informações, consulte [Instalação e configuração para Windows Gerenciamento Remoto.](installation-and-configuration-for-windows-remote-management.md)

Se seu script ou aplicativo exigir um método de autenticação específico que não está habilitado, você deverá alterar a configuração para habilitar esse tipo de autenticação. Essa alteração pode ser feita usando a ferramenta de linha de **comando winrm** ou Política de Grupo para o objeto **Windows Remote Management Política de Grupo .** Você também pode optar por desabilitar determinados métodos de autenticação.

**Para habilitar ou desabilitar a autenticação com a ferramenta Winrm**

1.  Para definir a configuração do cliente WinRM, use o **comando Winrm Set** e especifique o cliente. Por exemplo, o comando a seguir desabilita a autenticação digest para o cliente.

    **winrm set winrm/config/client/auth @{Digest="false"}**

2.  Para definir a configuração do servidor WinRM, use o **comando Winrm Set** e especifique o serviço. Por exemplo, o comando a seguir habilita a autenticação Kerberos para o serviço.

    **winrm set winrm/config/service/auth @{Kerberos="true"}**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> </dl>

 

 




