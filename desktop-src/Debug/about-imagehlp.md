---
description: As funções ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Sobre ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815646"
---
# <a name="about-imagehlp"></a>Sobre ImageHlp

As funções ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE. Todas as funções ImageHlp são de thread único. Portanto, chamadas de mais de um thread para essa função provavelmente resultarão em comportamento inesperado ou corrupção de memória. Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.

Os tópicos a seguir descrevem as imagens PE e a funcionalidade fornecida pelas funções ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funções de acesso à imagem](image-access-functions.md)
-   [Funções de integridade da imagem](image-integrity-functions.md)
-   [Funções de modificação de imagem](image-modification-functions.md)

 

 



