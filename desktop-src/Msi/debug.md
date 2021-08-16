---
description: Se essa política de sistema por computador estiver definida como &\# 0034;1&0034;, o instalador grava mensagens comuns de depuração no depurador usando a \# função OutputDebugString.
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

Se essa política [](system-policy.md) de sistema por computador estiver definida como "1", o instalador grava mensagens comuns de depuração no depurador usando a [**função OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Se esse valor for definido como "2", o instalador grava todas as mensagens de depuração válidas no depurador usando a [**função OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Essa política é apenas para fins de depuração e pode não ter suporte em versões futuras do Windows Installer.

Windows O instalador só grava linhas de comando no arquivo de log se o terceiro bit (0x04) estiver definido no valor da política de Depuração. Portanto, para exibir linhas de comando no log, depure o valor da política de depuração como 7. Isso não exibe propriedades associadas a um [Controle de Edição com](edit-control.md) o Atributo de Controle de [Senha](password-control-attribute.md). Isso tornará as propriedades definidas na linha de comando visíveis no log, mesmo que a propriedade seja incluída na [**propriedade MsiHiddenProperties.**](msihiddenproperties.md) Para obter mais informações, [consulte Impedindo que informações confidenciais são escritas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 
