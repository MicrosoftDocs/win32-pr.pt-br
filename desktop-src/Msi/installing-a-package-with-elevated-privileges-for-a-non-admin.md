---
description: Um administrador pode usar os métodos a seguir para permitir que um usuário não administrador instale um aplicativo com privilégios de sistema elevados.
ms.assetid: 61b9297e-f45e-4f50-9001-9bae580e1bf4
title: Instalando um pacote com privilégios elevados para um não administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81de333d6ca388017e03c96f739d7bd258a7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836993"
---
# <a name="installing-a-package-with-elevated-privileges-for-a-non-admin"></a>Instalando um pacote com privilégios elevados para um não administrador

Um administrador pode usar os métodos a seguir para permitir que um usuário não administrador instale um aplicativo com privilégios de sistema elevados.

-   No Windows Vista com Windows Installer, um membro do grupo Administradores pode fornecer autorização para que um não administrador eleve a instalação por meio do UAC ( [*controle de conta de usuário*](u-gly.md) ), conforme descrito em [usando Windows Installer com o UAC](using-windows-installer-with-uac.md).

    **Windows Vista:** Necessário.

Os métodos a seguir também podem ser usados para instalar um aplicativo com privilégios de sistema elevados.

-   Um administrador pode anunciar um aplicativo no computador de um usuário atribuindo ou publicando o pacote de Windows Installer usando a implantação e a [política de grupo](/previous-versions/windows/desktop/Policy/group-policy-start-page)de aplicativos. O administrador anuncia o pacote para instalação por máquina. Se um usuário não administrador instalar o aplicativo, a instalação poderá ser executada com privilégios elevados. Os usuários não administradores não podem instalar pacotes não anunciados que exigem privilégios de sistema elevados.
-   Um administrador pode acessar o computador do usuário e [anunciar](advertisement.md) o aplicativo para a instalação por máquina. Como a Windows Installer sempre tem privilégios elevados ao fazer instalações no [contexto de instalação](installation-context.md)por máquina, se um usuário não administrador instalar o aplicativo anunciado, a instalação poderá ser executada com privilégios elevados. Os usuários não administradores ainda não podem instalar pacotes não anunciados que exigem privilégios elevados.
-   Um usuário sem privilégios pode instalar um aplicativo anunciado que exige privilégios elevados se um agente do sistema local anunciar o aplicativo. O aplicativo pode ser anunciado para uma instalação por usuário ou por computador. Um aplicativo instalado usando esse método é considerado gerenciado. Para obter mais informações, consulte [anunciando um aplicativo Per-User a ser instalado com privilégios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md).
-   Um administrador pode definir a política de [AlwaysInstallElevated](alwaysinstallelevated.md) para instalações por usuário e por computador. Esse método pode abrir um computador para um risco de segurança, porque quando essa política é definida, um usuário não administrador pode executar instalações com privilégios elevados e acessar locais seguros no computador, como o SystemFolder ou a chave do registro **HKLM** .

    Se o aplicativo estiver instalado por computador enquanto a política [AlwaysInstallElevated](alwaysinstallelevated.md) estiver definida, o produto será tratado como gerenciado. Nesse caso, o aplicativo ainda poderá executar um reparo com privilégios elevados se a política for removida. Além disso, se o aplicativo for instalado por usuário enquanto a política AlwaysInstallElevated estiver definida, o aplicativo não poderá executar um reparo se a política for removida.

-   Um administrador pode acessar o computador de um usuário e fazer uma instalação por computador do aplicativo. Como os privilégios são necessários para executar esse tipo de instalação, as instalações por máquina são sempre gerenciadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contexto de instalação](installation-context.md)
</dt> </dl>

 

 
