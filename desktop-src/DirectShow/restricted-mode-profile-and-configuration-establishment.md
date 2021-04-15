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
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="84fb4-103">Perfil de modo restrito e estabelecimento de configuração</span><span class="sxs-lookup"><span data-stu-id="84fb4-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="84fb4-104">Devido à variedade de tipos de dados que podem ser decodificados pelo DirectX VA, e as várias configurações de decodificação com suporte no DirectX VA para cada um desses tipos de dados (por exemplo, usando buffers de fragmentado versus a decodificação de diferença do resíduo de host versus IDCT baseadas em acelerador com e sem criptografia de cada tipo de buffer relevante e assim por diante), acreditamos que seria um pouco não mais simples especificar um GUID exclusivo para cada tipo de dados e decodificação</span><span class="sxs-lookup"><span data-stu-id="84fb4-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="84fb4-105">Isso criaria um grande número de GUIDs (por exemplo, de forma hipotética, se havia 16 perfis de DirectX VA e 16 configurações possíveis para cada um, precisaria ter 256 GUIDs definidos, exigindo 4 kilobytes de memória apenas para manter todos eles.</span><span class="sxs-lookup"><span data-stu-id="84fb4-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="84fb4-106">Esse problema é a parte mais difícil de determinar como mapear o DirectX VA para o **IAMVideoAccelerator**, com o restante da definição operacional, na maioria das vezes muito simples.</span><span class="sxs-lookup"><span data-stu-id="84fb4-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="84fb4-107">Como resultado, especificamos um GUID exclusivo apenas para cada tipo de dados (para cada perfil de modo restrito) e permitem que um GUID adicional seja associado a cada tipo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="84fb4-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="84fb4-108">A configuração de decodificação é então estabelecida entre o decodificador e o acelerador por uma negociação subordinada de nível inferior usando operações de investigação e bloqueio para estabelecer configurações para cada tipo de função do DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="84fb4-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



