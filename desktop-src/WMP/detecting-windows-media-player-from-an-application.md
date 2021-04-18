---
title: Detectando o Windows Media Player de um aplicativo
description: Detectando o Windows Media Player de um aplicativo
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, detectando de aplicativos
- detectando o Windows Media Player de aplicativos
- registro, detectando o Windows Media Player de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ae0c7d30b71749a22ecef10806817cd4182224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810566"
---
# <a name="detecting-windows-media-player-from-an-application"></a>Detectando o Windows Media Player de um aplicativo

Você pode determinar qual versão do Windows Media Player está instalada verificando a seguinte chave do registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Active Setup \\ componentes instalados**

Para o Windows Media Player 6,4, consulte a chave **{22d6f312-b0f6-11D0-94ab-0080c74c7e95}**.

Para o Windows Media Player 7 ou posterior, consulte a chave **{6BF52A52-394A-11D3-B153-00C04F79FAA6}**.

Em qualquer uma dessas chaves, se o tiver sido **instalado** ,<dl> <dt>

Tipo de dados
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo de dados
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Redistribuindo o software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




