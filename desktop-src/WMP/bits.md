---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Armazenamentos online do Windows Media Player, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- tipo 2 lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- BITS
- BITS (Serviço de Transferência Inteligente em Segundo Plano)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294172"
---
# <a name="bits"></a><span data-ttu-id="35ad2-108">BITS</span><span class="sxs-lookup"><span data-stu-id="35ad2-108">BITS</span></span>

<span data-ttu-id="35ad2-109">O [serviço de transferência inteligente em segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) é um recurso do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="35ad2-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="35ad2-110">O BITS transfere arquivos (downloads ou uploads) entre um cliente e um servidor e fornece informações de progresso relacionadas às transferências.</span><span class="sxs-lookup"><span data-stu-id="35ad2-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="35ad2-111">Se você quiser transferir arquivos usando código C++, o BITS é a tecnologia correta a ser usada.</span><span class="sxs-lookup"><span data-stu-id="35ad2-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="35ad2-112">Se você quiser transferir arquivos usando código JScript em sua página da Web da loja online, use o Gerenciador de download em vez disso.</span><span class="sxs-lookup"><span data-stu-id="35ad2-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="35ad2-113">Como o Gerenciador de download do Windows Media Player usa BITS, você pode executar etapas para configurar seus trabalhos de cópia do BITS de forma que o Windows Media Player gerencie os trabalhos para você.</span><span class="sxs-lookup"><span data-stu-id="35ad2-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="35ad2-114">Para fazer isso, você deve seguir a Convenção descrita na seção [Convenção de trabalho do bits do Windows Media Player](windows-media-player-bits-job-convention.md) ao adicionar seus trabalhos à fila de transferência do bits.</span><span class="sxs-lookup"><span data-stu-id="35ad2-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="35ad2-115">Esta seção também descreve um mecanismo para recuperar informações sobre seus trabalhos do BITS em sua página da Web de lojas online.</span><span class="sxs-lookup"><span data-stu-id="35ad2-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35ad2-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35ad2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ad2-117">**Usando o Gerenciador de download**</span><span class="sxs-lookup"><span data-stu-id="35ad2-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="35ad2-118">**Sobre as lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="35ad2-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 