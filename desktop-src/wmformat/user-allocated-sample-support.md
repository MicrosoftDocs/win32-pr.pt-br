---
title: Suporte de amostra alocado pelo usuário
description: Suporte de amostra alocado pelo usuário
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- SDK do Windows Media Format, suporte de exemplo alocado pelo usuário
- ASF (Advanced Systems Format), suporte de amostra alocado pelo usuário
- ASF (formato de sistemas avançados), suporte de amostra alocado pelo usuário
- suporte de amostra alocado pelo usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005277"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="84ca5-107">Suporte de amostra alocado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="84ca5-107">User Allocated Sample Support</span></span>

<span data-ttu-id="84ca5-108">Em circunstâncias normais, o objeto leitor e o objeto leitor síncrono criam um novo objeto de buffer para cada amostra entregue ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84ca5-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="84ca5-109">Isso ocorre porque o objeto de leitura não tem como saber o que o seu aplicativo faz com os exemplos depois de obtê-los.</span><span class="sxs-lookup"><span data-stu-id="84ca5-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="84ca5-110">Embora muitos aplicativos leiam amostras apenas para processá-los imediatamente, alguns aplicativos podem precisar manter amostras por um longo tempo.</span><span class="sxs-lookup"><span data-stu-id="84ca5-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="84ca5-111">O objeto de leitura não pode, portanto, reutilizar qualquer um dos buffers que ele aloca; Ele os entrega para seu aplicativo, que então tem controle sobre eles.</span><span class="sxs-lookup"><span data-stu-id="84ca5-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="84ca5-112">O problema dessa abordagem é que um arquivo pode conter uma grande quantidade de amostras.</span><span class="sxs-lookup"><span data-stu-id="84ca5-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="84ca5-113">Se cada um deles exigir que um novo objeto de buffer seja criado, muito tempo de processador será desperdiçado alocando e liberando memória.</span><span class="sxs-lookup"><span data-stu-id="84ca5-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="84ca5-114">Em aplicativos com detecção de tempo, como media players, essa sobrecarga pode ser muito prejudicial para o desempenho.</span><span class="sxs-lookup"><span data-stu-id="84ca5-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="84ca5-115">Para aliviar os problemas de desempenho de amostras alocadas pelo leitor, o leitor e o leitor síncrono oferecem suporte a exemplos alocados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="84ca5-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="84ca5-116">Para usar exemplos alocados por seu aplicativo, o objeto de leitura faz chamadas para um método de retorno de chamada de alocação de exemplo que você implementa.</span><span class="sxs-lookup"><span data-stu-id="84ca5-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="84ca5-117">A lógica usada pelo retorno de chamada para entregar buffers ao objeto de leitura depende inteiramente de você.</span><span class="sxs-lookup"><span data-stu-id="84ca5-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="84ca5-118">Você pode usar um pool de buffers para todo o arquivo ou usar vários pools de buffers, um para cada saída ou fluxo ou qualquer outro esquema que funcione para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="84ca5-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84ca5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="84ca5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ca5-120">**Alocando buffers para leitura de arquivo**</span><span class="sxs-lookup"><span data-stu-id="84ca5-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="84ca5-121">**Recursos de leitura de arquivo**</span><span class="sxs-lookup"><span data-stu-id="84ca5-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




