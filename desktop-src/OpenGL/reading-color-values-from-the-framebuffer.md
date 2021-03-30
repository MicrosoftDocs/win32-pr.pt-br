---
title: Lendo valores de cor do framebuffer
description: Ao usar funções que lêem valores de cor de framebuffer, esteja atento às diferenças entre ler valores RGBA e valores de índice de cor em dispositivos true-color e em dispositivos baseados em paleta.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL no Windows, lendo valores de cor de framebuffers
- lendo valores de cor do framebuffers OpenGL
- framebuffers, lendo valores de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635521"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lendo valores de cor do framebuffer

Ao usar funções que lêem valores de cor de framebuffer, esteja atento às diferenças entre ler valores RGBA e valores de índice de cor em dispositivos true-color e em dispositivos baseados em paleta.

Em um dispositivo true-color:

-   Os valores RGBA são limitados ao canal no dispositivo.
-   Os valores de índice de cor são armazenados como valores RGBA no framebuffer. Ao usar esses valores, você deve executar uma conversão inversa de RGBA para o índice lógico de paleta. Se dois índices lógicos tiverem os mesmos valores RGBA, o índice incorreto poderá ser retornado.

Em um dispositivo baseado em paleta:

-   Os valores RGBA são lidos de um índice na paleta do sistema. O índice lógico é obtido de uma tabela inversa e os componentes RGBA são extraídos.
-   Os valores de índice de cor são lidos de um índice para a paleta do sistema e uma tabela inversa é usada para obter o índice lógico da paleta.

 

 




