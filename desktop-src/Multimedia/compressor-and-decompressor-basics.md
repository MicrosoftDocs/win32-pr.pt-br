---
title: Noções básicas de compressor e descompactador
description: Noções básicas de compressor e descompactador
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- VCM (Gerenciador de compactação de vídeo), abrindo compactadores
- VCM (Gerenciador de compactação de vídeo), abrindo compactadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822586"
---
# <a name="compressor-and-decompressor-basics"></a><span data-ttu-id="0a9a4-105">Noções básicas de compressor e descompactador</span><span class="sxs-lookup"><span data-stu-id="0a9a4-105">Compressor and Decompressor Basics</span></span>

<span data-ttu-id="0a9a4-106">Para abrir e localizar um compressor, você pode usar as funções [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) e [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) .</span><span class="sxs-lookup"><span data-stu-id="0a9a4-106">To open and locate a compressor, you can use the [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) and [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) functions.</span></span> <span data-ttu-id="0a9a4-107">Você pode usar o **ICLocate** para encontrar um compressor de um tipo específico e obter um identificador de ti para uso em outras funções do VCM.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-107">You can use **ICLocate** to find a compressor of a specific type and to obtain a handle of it for use in other VCM functions.</span></span> <span data-ttu-id="0a9a4-108">Para abrir um compressor, você pode usar **ICOpen**.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-108">To open a compressor, you can use **ICOpen**.</span></span> <span data-ttu-id="0a9a4-109">Seu aplicativo usa o identificador retornado por essa função para identificar o compactador aberto quando ele usa outras funções VCM.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-109">Your application uses the handle returned by this function to identify the opened compressor when it uses other VCM functions.</span></span>

<span data-ttu-id="0a9a4-110">Para abrir e localizar um descompactador, os aplicativos podem usar as macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) e [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) .</span><span class="sxs-lookup"><span data-stu-id="0a9a4-110">To open and locate a decompressor, applications can use the [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) and [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) macros.</span></span> <span data-ttu-id="0a9a4-111">Essas macros usam **ICLocate** para a operação.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-111">These macros use **ICLocate** for operation.</span></span>

<span data-ttu-id="0a9a4-112">Quando o aplicativo tiver terminado de usar um compactador ou descompactador, ele deverá fechá-lo para liberar todos os recursos usados para compactação ou descompactação.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-112">When your application has finished using a compressor or decompressor, it must close it to free any resources used for compression or decompression.</span></span> <span data-ttu-id="0a9a4-113">Seu aplicativo pode usar a função [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) para fechar o compressor ou o descompactador.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-113">Your application can use the [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) function to close the compressor or decompressor.</span></span>

<span data-ttu-id="0a9a4-114">Além disso, seu aplicativo pode enumerar os compactadores ou os decompactadores em um sistema usando a função [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="0a9a4-114">Also, your application can enumerate the compressors or decompressors on a system by using the [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) function.</span></span>

> [!Note]  
> <span data-ttu-id="0a9a4-115">O cabeçalho de fluxo em um arquivo AVI contém informações sobre o tipo de fluxo e o manipulador específico para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-115">The stream header in an AVI file contains information about the stream type and the specific handler for that stream.</span></span> <span data-ttu-id="0a9a4-116">Dentro do cabeçalho do fluxo, os membros **fccType** e **fccHandler** identificam o tipo de fluxo e o manipulador de fluxo especificado para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="0a9a4-116">Within the stream header, the **fccType** and **fccHandler** members identify the stream type and the stream handler specified for the stream.</span></span>

 

 

 




