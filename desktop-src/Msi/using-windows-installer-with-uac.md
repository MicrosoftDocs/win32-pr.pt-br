---
description: Windows O instalador está em conformidade com o UAC (Controle de Conta de Usuário) no Windows Vista.
ms.assetid: 13955ded-6b7f-475f-bb0f-6530a0b4963f
title: Usando Windows instalador com UAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458d6265938f44a694366e8145d60aa5d031d47e715932502bd1b82e7012b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942276"
---
# <a name="using-windows-installer-with-uac"></a>Usando Windows instalador com UAC

Windows O instalador está em conformidade [*com*](u-gly.md) o UAC (Controle de Conta de Usuário) no Windows Vista. Com a autorização de um administrador, o Windows instalador pode instalar aplicativos ou patches em nome de um usuário que pode não ser membro do grupo Administradores. Isso é chamado [](e-gly.md) de instalação elevada porque o instalador do Windows faz alterações no sistema em nome do usuário que normalmente não seriam permitidas se o usuário estivesse fazendo as alterações diretamente.

-   Ao usar Windows Vista em um ambiente corporativo, os aplicativos podem ser designados como aplicativos gerenciados. Usando a implantação de aplicativos [e Política de Grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page), os administradores podem bloquear diretórios e, em seguida, atribuir ou publicar os aplicativos gerenciados nesses diretórios para usuários padrão para instalação, reparo ou remoção. [](s-gly.md) Os aplicativos gerenciados são registrados no hive do registro **HKEY \_ LOCAL \_ MACHINE.** Depois que um aplicativo é registrado como um aplicativo gerenciado, as operações de instalação subsequentes sempre são executados com privilégios elevados. Se o usuário estiver executando como administrador, nenhuma solicitação será necessária para continuar a instalação. Se o usuário estiver em execução como um usuário padrão e o aplicativo já tiver sido atribuído ou publicado, a instalação do aplicativo gerenciado poderá continuar sem solicitar.
-   Ao usar Windows Vista em um ambiente não corporativo, o UAC lida com a elevação da instalação do aplicativo. Windows O Instalador 4.0 pode chamar o Serviço de [*Informações*](a-gly.md) do Aplicativo (AIS) para solicitar autorização de administrador para elevar uma instalação. Antes que uma instalação identificada como exigindo privilégios de administrador possa ser executado, o UAC solicita o consentimento do usuário para elevar a instalação. O prompt de consentimento é exibido por padrão, mesmo que o usuário seja um membro do grupo Administradores local, porque os administradores são executados como usuários padrão até que um aplicativo ou componente do sistema que exija permissão de solicitação de credencial administrativa seja executado. Essa experiência do usuário é chamada [*de Modo de Aprovação de*](a-gly.md) Administrador (AAM). Se um usuário padrão tentar instalar o aplicativo, o usuário terá que obter uma pessoa com privilégio de administrador para fornecer suas credenciais de administrador para continuar a instalação. Essa experiência do usuário é chamada de prompt de credencial OTS (Over [*the Shoulder).*](o-gly.md)
-   Como o UAC restringe privilégios durante os estágios de uma instalação, os desenvolvedores de pacotes do Windows Installer não devem supor que sua instalação sempre terá acesso a todas as partes do sistema. Windows Portanto, os desenvolvedores de pacotes do instalador devem seguir as diretrizes de pacote [descritas](guidelines-for-packages.md) em Diretrizes para pacotes para garantir que seu pacote funcione com OAC e Windows Vista. Um pacote que foi criado e testado para estar em conformidade com o UAC deve conter a propriedade [**MSIDEPLOYMENTCOMPLIANT**](msideploymentcompliant.md) definida como 1.
-   Um administrador também pode usar os métodos descritos na seção: Instalando um pacote com privilégios [elevados](installing-a-package-with-elevated-privileges-for-a-non-admin.md) para um não administrador para permitir que um usuário não administrador instale um aplicativo com privilégios elevados do sistema.
-   Os privilégios são necessários para instalar um aplicativo no contexto gerenciado por usuário e, portanto, as reinstalações ou reparos subsequentes do instalador do Windows do aplicativo também são executados pelo instalador usando privilégios elevados. Isso significa que somente patches de fontes confiáveis podem ser aplicados a um aplicativo no estado gerenciado por usuário. A partir do Windows 3.0, você pode aplicar um patch a um aplicativo gerenciado por usuário depois que o patch tiver sido registrado como tendo privilégios elevados. Para obter informações, [consulte Patching Per-User Managed Applications](patching-per-user-managed-applications.md).

> [!Note]  
> Quando privilégios elevados não são necessários para instalar um pacote do instalador do Windows, o autor do pacote pode suprimir a caixa de diálogo exibida pelo UAC para solicitar autorização de administrador aos usuários. Para obter mais informações, consulte [Authoring Packages without the UAC Dialog Box](authoring-packages-without-the-uac-dialog-box.md).

 

 

 
