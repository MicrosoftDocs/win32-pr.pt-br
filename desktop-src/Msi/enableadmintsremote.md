---
description: A partir do Windows Server 2008 e do Windows Vista, essa política não tem mais efeito.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165005"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

A partir do Windows Server 2008 e do Windows Vista, essa política não tem mais efeito. Um administrador pode executar uma instalação a partir da sessão de console de um servidor de terminal. Um administrador também pode executar uma instalação de uma sessão de cliente do servidor de terminal.

Para obter mais informações, consulte [serviços de terminal](/windows/desktop/TermServ/terminal-services-portal) no SDK (Software Development Kit) do Microsoft Windows.

* * Sistemas operacionais anteriores ao Windows Server 2008 e ao Windows Vista: * *

Definir essa [política de sistema](system-policy.md) por máquina permite que os administradores executem instalações de uma sessão de cliente do servidor de terminal. Se essa política não estiver definida, os administradores só poderão executar instalações da sessão de console. Usuários não administrativos nunca podem executar instalações de uma sessão de cliente. O valor padrão dessa política permite que somente os administradores executem instalações da sessão do console. Os administradores sempre podem fazer [instalações administrativas](administrative-installation.md) de uma sessão de cliente do servidor de terminal ou da sessão de console, independentemente de essa política ser definida.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte também, [usando Windows Installer com um Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
