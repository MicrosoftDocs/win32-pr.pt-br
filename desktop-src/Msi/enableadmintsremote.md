---
description: Começando com Windows Server 2008 e Windows Vista, essa política não tem mais nenhum efeito.
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

Começando com Windows Server 2008 e Windows Vista, essa política não tem mais nenhum efeito. Um administrador pode executar uma instalação da sessão de console de um servidor terminal. Um administrador também pode executar uma instalação de uma sessão de cliente do servidor terminal.

Para obter mais informações, [consulte Serviços de Terminal](/windows/desktop/TermServ/terminal-services-portal) no Microsoft Windows Software Development Kit (SDK).

**Sistemas operacionais anteriores ao Windows Server 2008 e Windows Vista: **

Definir essa política de sistema [por computador](system-policy.md) permite que os administradores executem instalações de uma sessão de cliente do servidor terminal. Se essa política não estiver definida, os administradores só poderão executar instalações da sessão do console. Usuários não administrativas nunca podem executar instalações de uma sessão do cliente. O valor padrão dessa política permite que somente os administradores executem instalações da sessão do console. Os administradores sempre podem fazer instalações [administrativas](administrative-installation.md) de uma sessão de cliente do servidor terminal ou da sessão do console, independentemente de essa política estar definida.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte [também Usando Windows instalador com um servidor de terminal.](using-windows-installer-with-a-terminal-server.md)

 

 
