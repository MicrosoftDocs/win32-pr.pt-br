---
description: Para ajudar a manter um ambiente seguro durante a instalação do software, siga estas diretrizes ao criar o pacote de Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Diretrizes para a criação de instalações seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d18e66c38480149ddad9e381c6461ffe50cf0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752653"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Diretrizes para a criação de instalações seguras

A adesão às seguintes diretrizes ao criar um pacote de Windows Installer ajuda a manter um ambiente seguro durante a instalação:

-   Os administradores devem instalar aplicativos gerenciados em uma pasta de instalação de destino para a qual os usuários não administradores não têm privilégios de alteração ou modificação.
-   Torne qualquer propriedade definida pelo usuário uma propriedade pública. As propriedades particulares não podem ser alteradas pelo usuário interagindo com a interface do usuário. Para obter informações, consulte [sobre propriedades](about-properties.md).
-   Não use Propriedades para senhas ou outras informações que devam permanecer seguras. O instalador pode gravar o valor de uma propriedade criada na tabela de [Propriedades](property-table.md)ou criado em tempo de execução, em um log ou no registro do sistema. Para obter informações adicionais, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Quando a instalação requer que o instalador use privilégios [*elevados*](e-gly.md) , use [Propriedades públicas restritas](restricted-public-properties.md) para restringir as propriedades públicas que um usuário pode alterar. Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios *elevados* .
-   Evite instalar serviços que representam os privilégios de um usuário específico, pois isso pode gravar dados de segurança em um log ou no registro do sistema. Isso cria potencial para um problema de segurança, conflito de senha ou perda de dados de configuração quando o sistema é reiniciado. Para obter detalhes, consulte a [tabela de instalação](serviceinstall-table.md).
-   Use a tabela [LockPermissions](lockpermissions-table.md) e a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) para proteger serviços, arquivos, chaves do registro e pastas criadas em um ambiente bloqueado.
-   Adicione assinaturas digitais à instalação para garantir a integridade dos arquivos. Para obter detalhes, consulte [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) e [criando uma instalação assinada totalmente verificada](authoring-a-fully-verified-signed-installation.md).
-   Crie seu pacote de Windows Installer de modo que, se o usuário tiver acesso negado aos recursos, a instalação falhará de uma maneira que mantenha um ambiente seguro. Verifique os privilégios de acesso do usuário e determine se há espaço em disco suficiente antes do início da instalação. Normalmente, o instalador só deve exibir uma caixa de diálogo de procura se o usuário atual for um administrador ou se a instalação não exigir privilégios [*elevados*](e-gly.md) . Para obter detalhes, consulte [resiliência de origem](source-resiliency.md).
-   Use [transformações protegidas](secured-transforms.md) para armazenar transformações em um sistema de arquivos seguro localmente no computador do usuário. Isso impede que o usuário tenha acesso de gravação à transformação.
-   Para obter informações sobre como proteger as fontes de mídia de aplicativos gerenciados, consulte [resiliência de origem](source-resiliency.md).
-   Use a propriedade [**Resumo de segurança**](security-summary.md) para indicar se o pacote deve ser aberto como somente leitura. Essa propriedade deve ser definida como somente leitura recomendada para um banco de dados de instalação e para somente leitura imposta para uma transformação ou um patch.
-   O instalador executa ações personalizadas com privilégios de usuário por padrão para limitar o acesso de ações personalizadas ao sistema. O instalador pode executar ações personalizadas com privilégios [*elevados*](e-gly.md) se um aplicativo gerenciado estiver sendo instalado ou se a política do sistema tiver sido especificada para privilégios elevados. Para obter detalhes, consulte [segurança de ação personalizada](custom-action-security.md).
-   Use a política [DisablePatch](disablepatch.md) para fornecer segurança em ambientes em que a aplicação de patch deve ser restrita.
-   Use a [tabela AppID](appid-table.md) para registrar configurações comuns de segurança e configuração para objetos DCOM.
-   Para obter informações relacionadas, consulte [diretrizes para proteger ações personalizadas](guidelines-for-securing-custom-actions.md).
-   Para obter informações relacionadas, consulte [diretrizes para proteger pacotes em computadores bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md).
-   A partir do Windows Installer 3,0, a [aplicação de patches do UAC (controle de conta de usuário)](user-account-control--uac--patching.md) permite que usuários não administradores corrijam aplicativos instalados no contexto por máquina. A aplicação de patches do UAC é habilitada fornecendo um certificado de signatário na tabela [MsiPatchCertificate](msipatchcertificate-table.md) e patches de assinatura com o mesmo certificado.
-   A capacidade do Windows Installer 5,0 de definir permissões de acesso em serviços, arquivos, pastas criadas e entradas de registro pode ajudar a tornar os aplicativos de instalação mais seguros. Para obter informações, consulte [Securing Resources](securing-resources-.md).

 

 



