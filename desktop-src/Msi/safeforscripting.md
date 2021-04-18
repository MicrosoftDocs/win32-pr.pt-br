---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador não avisará os usuários quando os scripts em uma página da Web usarem a interface de automação do instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756891"
---
# <a name="safeforscripting"></a>SafeForScripting

Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador não avisará os usuários quando os scripts em uma página da Web usarem a [interface de automação](automation-interface.md)do instalador.

Antes de definir essa política, você deve considerar se, antes do prompt do usuário, ele fornece um nível apropriado de segurança para seus usuários. Se essa política não estiver definida, quando um script hospedado por um navegador da Internet tentar instalar um aplicativo, o sistema avisará o usuário e solicitará que eles aceitem ou recusem a instalação. A definição de SafeForScripting suprime esse aviso e pode permitir a instalação de aplicativos no sistema sem o conhecimento do usuário. Essa política pode ser útil para uma empresa que usa ferramentas baseadas na Web para distribuir programas.

Para obter mais informações, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) e [baixar uma instalação da Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



