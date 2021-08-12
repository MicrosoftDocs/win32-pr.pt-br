---
title: detectando Windows Media Player de um aplicativo
description: detectando Windows Media Player de um aplicativo
ms.assetid: 3cf8a619-3b7e-45af-af6b-4711a45c7e07
keywords:
- Windows Media Player, detectando de aplicativos
- detectando Windows Media Player de aplicativos
- registro, detectando Windows Media Player de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5267dc6c3202d9ecf894377899dfb34cf02ad42dfee05f8d42896c39ae48fc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579482"
---
# <a name="detecting-windows-media-player-from-an-application"></a>detectando Windows Media Player de um aplicativo

você pode determinar qual versão do Windows Media Player está instalada verificando a seguinte chave do registro:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Active Setup \\ componentes instalados**

para Windows Media Player 6,4, consulte a chave **{22d6f312-b0f6-11d0-94ab-0080c74c7e95}**.

para Windows Media Player 7 ou posterior, consulte a chave **{6BF52A52-394A-11d3-B153-00C04F79FAA6}**.

Em qualquer uma dessas chaves, se o tiver sido **instalado** ,<dl> <dt>

Tipo de dados
</dt> <dd>DWORD</dd> </dl> DWORD value is set to 0x1, you can safely use the **Version**<dl> <dt>

Tipo de dados
</dt> <dd>string</dd> </dl> string value as the version of Windows Media Player that is installed.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**redistribuindo Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




