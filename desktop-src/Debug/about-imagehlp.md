---
description: As funções de ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Sobre o ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756225"
---
# <a name="about-imagehlp"></a>Sobre o ImageHlp

As funções de ImageHlp são usadas principalmente por ferramentas de programação, utilitários de instalação de aplicativos e outros programas que precisam de acesso aos dados contidos em uma imagem PE. Todas as funções de ImageHlp são thread único. Portanto, as chamadas de mais de um thread para essa função provavelmente resultarão em um comportamento inesperado ou corrupção de memória. Para evitar isso, você deve sincronizar todas as chamadas simultâneas de mais de um thread para essa função.

Os tópicos a seguir descrevem as imagens do PE e a funcionalidade fornecida pelas funções do ImageHlp.

-   [Formato PE](pe-format.md)
-   [Funções de acesso a imagens](image-access-functions.md)
-   [Funções de integridade da imagem](image-integrity-functions.md)
-   [Funções de modificação de imagem](image-modification-functions.md)

 

 



