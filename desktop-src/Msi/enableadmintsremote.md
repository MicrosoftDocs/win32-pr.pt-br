---
description: a partir do Windows Server 2008 e Windows Vista, essa política não tem mais efeito.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a644e6f0cb9200fd8a130a2cdb293e7658e3354b817f7378571fae0ab3b4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637100"
---
# <a name="enableadmintsremote"></a>EnableAdminTSRemote

a partir do Windows Server 2008 e Windows Vista, essa política não tem mais efeito. Um administrador pode executar uma instalação a partir da sessão de console de um servidor de terminal. Um administrador também pode executar uma instalação de uma sessão de cliente do servidor de terminal.

para obter mais informações, consulte [serviços de Terminal](/windows/desktop/TermServ/terminal-services-portal) no SDK (Software Development Kit) do Microsoft Windows.

* * sistemas operacionais anteriores ao Windows Server 2008 e Windows Vista: * *

Definir essa [política de sistema](system-policy.md) por máquina permite que os administradores executem instalações de uma sessão de cliente do servidor de terminal. Se essa política não estiver definida, os administradores só poderão executar instalações da sessão de console. Usuários não administrativos nunca podem executar instalações de uma sessão de cliente. O valor padrão dessa política permite que somente os administradores executem instalações da sessão do console. Os administradores sempre podem fazer [instalações administrativas](administrative-installation.md) de uma sessão de cliente do servidor de terminal ou da sessão de console, independentemente de essa política ser definida.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer** de políticas de Software de computador LOCAL

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

para obter mais informações, consulte também, [usando Windows Installer com um Terminal Server](using-windows-installer-with-a-terminal-server.md).

 

 
