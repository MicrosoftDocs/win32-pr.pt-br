---
description: Instale um pacote de Windows Installer com privilégios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505802"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Você pode usar a política AlwaysInstallElevated para instalar um pacote de Windows Installer com privilégios elevados (sistema).

* * Aviso: * *

Essa opção é equivalente a conceder direitos administrativos completos, o que pode representar um grande risco de segurança. A Microsoft não incentiva fortemente o uso dessa configuração.

Para instalar um pacote com privilégios elevados (sistema), defina o valor de AlwaysInstallElevated como "1" em ambas as seguintes chaves do registro:

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Se o valor de AlwaysInstallElevated não estiver definido como "1" em ambas as chaves de registro anteriores, o instalador usará privilégios elevados para instalar aplicativos gerenciados e usará o nível de privilégio do usuário atual para aplicativos não gerenciados.

Como essa política permite que os usuários instalem aplicativos que exigem acesso a diretórios e chaves do registro para os quais o usuário pode não ter permissão para exibir ou alterar, você deve considerar se ele fornece um nível apropriado de segurança aos usuários. Definir essa política direciona Windows Installer para usar permissões do sistema ao instalar o aplicativo no sistema. Se essa política não estiver definida, os aplicativos não distribuídos pelo administrador serão instalados usando os privilégios do usuário e somente os aplicativos gerenciados terão privilégios elevados.

Observe que, depois que a política por máquina para AlwaysInstallElevated estiver habilitada, qualquer usuário poderá definir sua configuração por usuário.

## <a name="remarks"></a>Comentários

Para obter informações sobre a interação dessa política com as fontes de instalação, consulte [Gerenciando fontes de instalação](managing-installation-sources.md).

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



