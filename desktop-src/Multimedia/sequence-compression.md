---
title: Compactação de sequência
description: Compactação de sequência
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- VCM (Gerenciador de compactação de vídeo), compactação de sequência
- VCM (Gerenciador de compactação de vídeo), compactação de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916220"
---
# <a name="sequence-compression"></a><span data-ttu-id="7f43b-105">Compactação de sequência</span><span class="sxs-lookup"><span data-stu-id="7f43b-105">Sequence Compression</span></span>

<span data-ttu-id="7f43b-106">Seu aplicativo pode usar as funções [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)e [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) para compactar uma sequência de quadros.</span><span class="sxs-lookup"><span data-stu-id="7f43b-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="7f43b-107">Essas funções usam os dados armazenados na estrutura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) .</span><span class="sxs-lookup"><span data-stu-id="7f43b-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="7f43b-108">Os aplicativos usam a função [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para permitir que o usuário selecione um compressor, abra-o e defina os parâmetros de compactação na estrutura **COMPVARS** ; no entanto, os aplicativos podem definir os parâmetros na estrutura manualmente.</span><span class="sxs-lookup"><span data-stu-id="7f43b-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="7f43b-109">Antes que um aplicativo possa começar a compactar uma sequência de quadros, ele deve usar **ICSeqCompressFrameStart** para alocar os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="7f43b-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="7f43b-110">Depois que os recursos são alocados, o aplicativo pode usar **ICSeqCompressFrame** para compactar cada quadro individualmente.</span><span class="sxs-lookup"><span data-stu-id="7f43b-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="7f43b-111">A taxa de quadros e a frequência de quadro chave usados na compactação da sequência são especificadas em membros da estrutura **COMPVARS** .</span><span class="sxs-lookup"><span data-stu-id="7f43b-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="7f43b-112">O valor de retorno para **ICSeqCompressFrame** aponta para os dados compactados.</span><span class="sxs-lookup"><span data-stu-id="7f43b-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="7f43b-113">Quando um aplicativo conclui a compactação de uma sequência, ele pode usar o **ICSeqCompressFrameEnd** para liberar recursos do sistema alocados para **ICSeqCompressFrameStart**.</span><span class="sxs-lookup"><span data-stu-id="7f43b-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="7f43b-114">Para liberar os recursos alocados para a estrutura **COMPVARS** , o aplicativo pode usar a função [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .</span><span class="sxs-lookup"><span data-stu-id="7f43b-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




