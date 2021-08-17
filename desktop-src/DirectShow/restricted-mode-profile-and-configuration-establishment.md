---
description: Perfil de modo restrito e estabelecimento de configuração
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Perfil de modo restrito e estabelecimento de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747046"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Perfil de modo restrito e estabelecimento de configuração

Devido à variedade de tipos de dados que podem ser decodificados pelo DirectX VA e as várias configurações de decodificação com suporte no DirectX VA para cada um desses tipos de dados (por exemplo, usando buffers bitstream versus decodificação de diferença residual de host versus IDCT baseado em acelerador com e sem criptografia de cada tipo relevante de buffer e assim por diante),  acreditamos que seria um pouco simples simplesmente especificar um GUID exclusivo para cada tipo de dados exclusivo e configuração de decodificação. Isso criaria um grande número de GUIDs (por exemplo, hipoteticamente, se houvesse 16 perfis de VA do DirectX e 16 configurações possíveis para cada um, precisaria haver 256 GUIDs definidos– exigindo 4 quilobytes de memória apenas para mantê-los todos. Esse problema é a parte mais difícil de determinar como mapear o DirectX VA para **IAMVideoAccelerator**, com o restante da definição operacional sendo bastante simples. Como resultado, especificamos um GUID exclusivo somente para cada tipo de dados (para cada perfil de modo restrito) e permitimos que um GUID adicional seja associado a cada tipo de criptografia. A configuração de decodificação é estabelecida entre o decodificador e o acelerador por uma negociação subordinada de nível inferior usando operações de investigação e bloqueio para estabelecer configurações para cada tipo de função VA do DirectX.

 

 



