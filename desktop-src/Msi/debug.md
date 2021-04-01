---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador gravará mensagens de depuração comuns no depurador usando a função OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829011"
---
# <a name="debug"></a>Depurar

Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador gravará mensagens de depuração comuns no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Se esse valor for definido como "2", o instalador gravará todas as mensagens de depuração válidas no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Essa política destina-se apenas para fins de depuração e pode não ter suporte em versões futuras do Windows Installer.

Windows Installer apenas grava linhas de comando no arquivo de log se o terceiro bit (0x04) estiver definido no valor da política de depuração. Portanto, para exibir linhas de comando no log, defina o valor da política de depuração como 7. Isso não exibe as propriedades associadas a um [controle de edição](edit-control.md) com o [atributo de controle de senha](password-control-attribute.md). Isso fará com que as propriedades definidas na linha de comando sejam visíveis no log, mesmo que a propriedade seja incluída na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) . Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 
