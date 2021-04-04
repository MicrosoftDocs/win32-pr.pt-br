---
title: Gerando um formato não padrão
description: Gerando um formato não padrão
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Gerenciador de compactação de áudio (ACM), formatos não padrão
- ACM (Gerenciador de compactação de áudio), formatos não padrão
- Exemplos do ACM, formatos não padrão
- função acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822584"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="15758-107">Gerando um formato não padrão</span><span class="sxs-lookup"><span data-stu-id="15758-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="15758-108">Às vezes, um aplicativo precisa de um formato não padrão.</span><span class="sxs-lookup"><span data-stu-id="15758-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="15758-109">Por exemplo, um aplicativo pode precisar de um arquivo de formato ADPCM de 16 kHz.</span><span class="sxs-lookup"><span data-stu-id="15758-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="15758-110">Como 16 kHz não é padrão, as funções de enumeração não irão gerar esse formato.</span><span class="sxs-lookup"><span data-stu-id="15758-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="15758-111">Na verdade, a codificação personalizada dos algoritmos de formato para o aplicativo não é uma maneira confiável de gerar um formato não padrão.</span><span class="sxs-lookup"><span data-stu-id="15758-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="15758-112">Às vezes é possível, no entanto, gerar um formato análogo Configurando um formato PCM válido com todas as informações necessárias e, em seguida, usando a função [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) .</span><span class="sxs-lookup"><span data-stu-id="15758-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="15758-113">Como os compactadores e os descompactadores tentam sugerir um formato mais próximo do formato desejado, o número de canais e a frequência são geralmente preservados.</span><span class="sxs-lookup"><span data-stu-id="15758-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




