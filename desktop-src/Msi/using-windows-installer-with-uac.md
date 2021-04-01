---
description: Windows Installer está em conformidade com o UAC (controle de conta de usuário) no Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Usando Windows Installer com o UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a05dcd2fb33eff24fb17702af1cb306f81002d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090930"
---
# <a name="using-windows-installer-with-uac"></a>Usando Windows Installer com o UAC

Windows Installer está em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ) no Windows Vista. Com a autorização de um administrador, o Windows Installer pode instalar aplicativos ou patches em nome de um usuário que pode não ser um membro do grupo de administradores. Isso é conhecido como uma instalação [*elevada*](e-gly.md) porque o Windows Installer faz alterações no sistema em nome do usuário que normalmente não seria permitido se o usuário estivesse fazendo as alterações diretamente.

-   Ao usar o Windows Vista em um ambiente corporativo, os aplicativos podem ser designados como aplicativos gerenciados. Usando a implantação e a [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page)de aplicativos, os administradores podem bloquear diretórios e, em seguida, atribuir ou publicar os aplicativos gerenciados nesses diretórios para [*usuários padrão*](s-gly.md) para instalação, reparo ou remoção. Os aplicativos gerenciados são registrados no hive do registro do **\_ \_ computador local hKey** . Depois que um aplicativo tiver sido registrado como um aplicativo gerenciado, as operações de instalação subsequentes sempre são executadas com privilégios elevados. Se o usuário estiver executando como administrador, nenhuma solicitação será necessária para continuar a instalação. Se o usuário estiver sendo executado como usuário padrão e o aplicativo já tiver sido atribuído ou publicado, a instalação do aplicativo gerenciado poderá continuar sem avisar.
-   Ao usar o Windows Vista em um ambiente não corporativo, o UAC lida com a elevação da instalação do aplicativo. Windows Installer 4,0 pode chamar o AIS ( [*serviço de informações de aplicativo*](a-gly.md) ) para solicitar a autorização do administrador para elevar uma instalação. Antes que uma instalação identificada como exigir privilégios de administrador possa ser executada, o UAC solicita ao usuário o consentimento para elevar a instalação. A solicitação de consentimento é exibida por padrão, mesmo que o usuário seja membro do grupo local de administradores, porque os administradores são executados como usuários padrão até um componente de aplicativo ou sistema que exige permissão de solicitações de credenciais administrativas para ser executado. Essa experiência do usuário é chamada de AAM ( [*modo de aprovação de administrador*](a-gly.md) ). Se um usuário padrão tentar instalar o aplicativo, o usuário precisará obter um privilégio de administrador para fornecer a eles suas credenciais de administrador para continuar a instalação. Essa experiência do usuário é chamada de solicitação de credencial (OTS) [*ao longo do ressalto*](o-gly.md) .
-   Como o UAC restringe os privilégios durante os estágios de uma instalação, os desenvolvedores de Windows Installer pacotes não devem pressupor que sua instalação sempre terá acesso a todas as partes do sistema. Os desenvolvedores de pacotes Windows Installer devem, portanto, aderir às diretrizes de pacote descritas em [diretrizes para pacotes](guidelines-for-packages.md) para garantir que seu pacote funcione com o UAC e o Windows Vista. Um pacote que foi criado e testado para estar em conformidade com o UAC deve conter a propriedade [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) definida como 1.
-   Um administrador também pode usar os métodos descritos na seção: [instalando um pacote com privilégios elevados para que um não](installing-a-package-with-elevated-privileges-for-a-non-admin.md) administrador habilite um usuário que não seja administradores para instalar um aplicativo com privilégios de sistema elevados.
-   Os privilégios são necessários para instalar um aplicativo no contexto gerenciado por usuário e, portanto, subsequentes Windows Installer reinstalações ou reparos do aplicativo também são executadas pelo instalador usando privilégios elevados. Isso significa que somente os patches de fontes confiáveis podem ser aplicados a um aplicativo no estado gerenciado por usuário. A partir do Windows Installer 3,0, você pode aplicar um patch a um aplicativo gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados. Para obter informações, consulte [aplicação de patches Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).

> [!Note]  
> Quando privilégios elevados não são necessários para instalar um pacote de Windows Installer, o autor do pacote pode suprimir a caixa de diálogo que o UAC exibe para solicitar aos usuários a autorização do administrador. Para obter mais informações, consulte [criando pacotes sem a caixa de diálogo UAC](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
