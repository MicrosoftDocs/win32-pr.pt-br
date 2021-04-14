---
title: Criando fluxos temporários
description: Criando fluxos temporários
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Função AVIStreamCreate
- Função AVIStreamRelease
- Função AVIMakeCompressedStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453584"
---
# <a name="creating-temporary-streams"></a><span data-ttu-id="1309a-106">Criando fluxos temporários</span><span class="sxs-lookup"><span data-stu-id="1309a-106">Creating Temporary Streams</span></span>

<span data-ttu-id="1309a-107">Os fluxos temporários podem ser benéficos de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="1309a-107">Temporary streams can be beneficial in several ways.</span></span> <span data-ttu-id="1309a-108">Você pode usar um fluxo temporário como um fluxo de trabalho, por exemplo, ao alterar o formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1309a-108">You can use a temporary stream as a work stream, for example, when changing the stream format.</span></span> <span data-ttu-id="1309a-109">Ou você pode criar um fluxo temporário para manter partes de outros fluxos que foram copiados.</span><span class="sxs-lookup"><span data-stu-id="1309a-109">Or you can create a temporary stream to hold portions of other streams that have been copied.</span></span>

<span data-ttu-id="1309a-110">Você pode criar um fluxo na memória que não esteja associado a nenhum arquivo usando a função [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) .</span><span class="sxs-lookup"><span data-stu-id="1309a-110">You can create a stream in memory that is not associated with any file by using the [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) function.</span></span> <span data-ttu-id="1309a-111">Essa função retorna o endereço da interface para o novo fluxo em um local especificado e é usada internamente por outras funções que criam fluxos temporários.</span><span class="sxs-lookup"><span data-stu-id="1309a-111">This function returns the address of the interface to the new stream in a specified location and is used internally by other functions that create temporary streams.</span></span>

<span data-ttu-id="1309a-112">Você pode criar um fluxo compactado a partir de um fluxo não compactado usando a função [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) .</span><span class="sxs-lookup"><span data-stu-id="1309a-112">You can create a compressed stream from an uncompressed stream by using the [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) function.</span></span> <span data-ttu-id="1309a-113">Você identifica o fluxo a ser compactado, o método de compactação e as opções de compactação e o manipulador para o novo fluxo.</span><span class="sxs-lookup"><span data-stu-id="1309a-113">You identify the stream to compress, the compression method and compression options, and the handler for the new stream.</span></span>

<span data-ttu-id="1309a-114">Quando você terminar de usar um fluxo criado com **AVIStreamCreate** ou **AVIMakeCompressedStream**, feche o fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) .</span><span class="sxs-lookup"><span data-stu-id="1309a-114">When you finish using a stream created with **AVIStreamCreate** or **AVIMakeCompressedStream**, close the stream by using the [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) function.</span></span> <span data-ttu-id="1309a-115">O **AVIStreamRelease** libera os recursos usados pelo fluxo temporário.</span><span class="sxs-lookup"><span data-stu-id="1309a-115">**AVIStreamRelease** frees the resources the temporary stream used.</span></span>

 

 




