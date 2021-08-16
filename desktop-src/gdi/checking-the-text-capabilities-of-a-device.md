---
description: Você pode usar as funções EnumFonts e EnumFontFamilies para enumerar as fontes disponíveis em um contexto de dispositivo de memória compatível com impressora.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Verificando os recursos de texto de um dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7121e7b5e2a416d06d79dba33c9a7c2eb7f6fb26d766a30b383f024e87e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354846"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Verificando os recursos de texto de um dispositivo

Você pode usar as funções [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) e [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) para enumerar as fontes disponíveis em um contexto de dispositivo de memória compatível com impressora. Você também pode usar a [função GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar informações sobre os recursos de texto de um dispositivo. Ao chamar a [**função GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) com o índice NUMFONTS, você pode determinar o número mínimo de fontes com suporte de uma impressora. (Uma impressora individual pode dar suporte a mais fontes do que o especificado no valor de retorno de **GetDeviceCaps** com o índice NUMFONTS.) Usando o índice TEXTCAPS, você pode identificar muitos dos recursos de texto do dispositivo especificado.

 

 
