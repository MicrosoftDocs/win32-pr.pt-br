---
description: Essa política do sistema por máquina pode ser usada para especificar que o Windows Installer passar todas as propriedades públicas para o lado do servidor durante uma instalação gerenciada usando privilégios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091139"
---
# <a name="enableusercontrol"></a>EnableUserControl

No caso de uma instalação gerenciada, o autor do pacote pode precisar limitar quais propriedades públicas são passadas para o lado do servidor e podem ser alteradas por um usuário que não seja um administrador do sistema. Algumas restrições são comumente necessárias para manter um ambiente seguro quando a instalação requer que o instalador use privilégios elevados.

Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador poderá passar todas as [Propriedades públicas](public-properties.md) para o lado do servidor durante uma instalação gerenciada usando privilégios elevados. Definir essa política tem o mesmo efeito que definir a propriedade **EnableUserControl** . Definir essa política permite que todas as propriedades públicas sejam passadas para o serviço e sejam alteradas por usuários não administrativos. Por padrão, essa política não está habilitada; somente as propriedades públicas restritas são passadas para o lado do servidor e podem ser alteradas por um usuário não administrativo. Todas as outras propriedades públicas são ignoradas.

Se o sistema operacional for o Windows 2000, o usuário não é um administrador do sistema e o aplicativo ou produto está sendo instalado com privilégios elevados, e um usuário que não é um administrador do sistema só pode substituir uma lista aprovada de propriedades públicas restritas. Para obter mais informações, consulte [Propriedades públicas restritas](restricted-public-properties.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



