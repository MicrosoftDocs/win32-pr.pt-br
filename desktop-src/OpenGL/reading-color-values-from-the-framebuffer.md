---
title: Lendo valores de cor do Framebuffer
description: Ao usar funções que leem novamente valores de cor do framebuffer, esteja ciente das diferenças entre ler valores RGBA e valores de índice de cores em dispositivos de cor verdadeira e em dispositivos baseados em paleta.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL no Windows, lendo valores de cor de framebuffers
- lendo valores de cores de framebuffers OpenGL
- framebuffers, leitura de valores de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65beb6dae04019637fc8683220ce12e671c4a52d4f015ae9f8d45e70db67bb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794763"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lendo valores de cor do Framebuffer

Ao usar funções que leem novamente valores de cor do framebuffer, esteja ciente das diferenças entre ler valores RGBA e valores de índice de cores em dispositivos de cor verdadeira e em dispositivos baseados em paleta.

Em um dispositivo de cor verdadeira:

-   Os valores de RGBA são limitados ao canal no dispositivo.
-   Os valores de índice de cor são armazenados como valores RGBA no framebuffer. Ao usar esses valores, você deve executar uma conversão inversa de RGBA para o índice de paleta lógica. Se dois índices lógicos têm os mesmos valores RGBA, o índice errado pode ser retornado.

Em um dispositivo baseado em paleta:

-   Os valores RGBA são lidos de um índice na paleta do sistema. O índice lógico é obtido de uma tabela inversa e os componentes RGBA são extraídos.
-   Os valores de índice de cor são lidos de um índice na paleta do sistema e uma tabela inversa é usada para obter o índice da paleta lógica.

 

 




