---
description: essa política do sistema por máquina pode ser usada para especificar que o Windows Installer passar todas as propriedades públicas para o lado do servidor durante uma instalação gerenciada usando privilégios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d8c56b1ea4d161030b252141e1930bd8298cea98b52b09511175d132e6a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637002"
---
# <a name="enableusercontrol"></a>EnableUserControl

No caso de uma instalação gerenciada, o autor do pacote pode precisar limitar quais propriedades públicas são passadas para o lado do servidor e podem ser alteradas por um usuário que não seja um administrador do sistema. Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios elevados.

Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador poderá passar todas as [Propriedades públicas](public-properties.md) para o lado do servidor durante uma instalação gerenciada usando privilégios elevados. Definir essa política tem o mesmo efeito que definir a propriedade **EnableUserControl** . Definir essa política permite que todas as propriedades públicas sejam passadas para o serviço e sejam alteradas por usuários não administrativos. Por padrão, essa política não está habilitada; somente as propriedades públicas restritas são passadas para o lado do servidor e podem ser alteradas por um usuário não administrativo. Todas as outras propriedades públicas são ignoradas.

se o sistema operacional for Windows 2000, o usuário não é um administrador do sistema e o aplicativo ou produto está sendo instalado com privilégios elevados, então um usuário que não é um administrador do sistema só pode substituir uma lista aprovada de propriedades públicas restritas. Para obter mais informações, consulte [Propriedades públicas restritas](restricted-public-properties.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer** de políticas de Software de computador LOCAL

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



