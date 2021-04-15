---
description: Perfil de modo restrito e estabelecimento de configuração
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Perfil de modo restrito e estabelecimento de configuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370157"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Perfil de modo restrito e estabelecimento de configuração

Devido à variedade de tipos de dados que podem ser decodificados pelo DirectX VA, e as várias configurações de decodificação com suporte no DirectX VA para cada um desses tipos de dados (por exemplo, usando buffers de fragmentado versus a decodificação de diferença do resíduo de host versus IDCT baseadas em acelerador com e sem criptografia de cada tipo de buffer relevante e assim por diante), acreditamos que seria um pouco não mais simples especificar um GUID exclusivo para cada tipo de dados e decodificação Isso criaria um grande número de GUIDs (por exemplo, de forma hipotética, se havia 16 perfis de DirectX VA e 16 configurações possíveis para cada um, precisaria ter 256 GUIDs definidos, exigindo 4 kilobytes de memória apenas para manter todos eles. Esse problema é a parte mais difícil de determinar como mapear o DirectX VA para o **IAMVideoAccelerator**, com o restante da definição operacional, na maioria das vezes muito simples. Como resultado, especificamos um GUID exclusivo apenas para cada tipo de dados (para cada perfil de modo restrito) e permitem que um GUID adicional seja associado a cada tipo de criptografia. A configuração de decodificação é então estabelecida entre o decodificador e o acelerador por uma negociação subordinada de nível inferior usando operações de investigação e bloqueio para estabelecer configurações para cada tipo de função do DirectX VA.

 

 



