---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador gravará mensagens de depuração comuns no depurador usando a função OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692866"
---
# <a name="debug"></a>Depurar

Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador gravará mensagens de depuração comuns no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Se esse valor for definido como "2", o instalador gravará todas as mensagens de depuração válidas no depurador usando a função [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . essa política destina-se apenas para fins de depuração e pode não ter suporte em versões futuras do Windows Installer.

Windows O instalador só gravará linhas de comando no arquivo de log se o terceiro bit (0x04) estiver definido no valor da política de depuração. Portanto, para exibir linhas de comando no log, defina o valor da política de depuração como 7. Isso não exibe as propriedades associadas a um [controle de edição](edit-control.md) com o [atributo de controle de senha](password-control-attribute.md). Isso fará com que as propriedades definidas na linha de comando sejam visíveis no log, mesmo que a propriedade seja incluída na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) . Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer** de políticas de Software de computador LOCAL

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 
