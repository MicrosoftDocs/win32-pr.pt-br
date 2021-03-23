---
title: Copiar descritores
description: Os métodos ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple na interface do dispositivo usam a CPU para copiar descritores imediatamente.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104525"
---
# <a name="copying-descriptors"></a><span data-ttu-id="6e0ab-103">Copiar descritores</span><span class="sxs-lookup"><span data-stu-id="6e0ab-103">Copying Descriptors</span></span>

<span data-ttu-id="6e0ab-104">Os métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) na interface do dispositivo usam a CPU para copiar imediatamente os descritores.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-104">The [**ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) and [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) methods on the device interface use the CPU to immediately copy descriptors.</span></span> <span data-ttu-id="6e0ab-105">Eles podem ser chamados de threads livres desde que vários threads na CPU ou GPU não executem gravações potencialmente conflitantes.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-105">They can be called free threaded as long as multiple threads on the CPU or GPU do not perform any potentially conflicting writes.</span></span>

## <a name="copying-descriptors-immediately-cpu-timeline"></a><span data-ttu-id="6e0ab-106">Copiando descritores imediatamente (linha do tempo de CPU)</span><span class="sxs-lookup"><span data-stu-id="6e0ab-106">Copying Descriptors Immediately (CPU Timeline)</span></span>

<span data-ttu-id="6e0ab-107">O número de descritores de origem (para copiar de), especificado como um conjunto de intervalos de descrição, deve ser igual ao número de descritores de destino (para copiar), especificado como um conjunto separado de intervalos de descritores.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-107">The number of source descriptors (to copy from), specified as a set of descriptor ranges, must equal the number of destination descriptors (to copy to), specified as a separate set of descriptor ranges.</span></span> <span data-ttu-id="6e0ab-108">Caso contrário, os intervalos de origem e de destino não precisam ser alinhados.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-108">The source and destination ranges do not otherwise have to line up.</span></span> <span data-ttu-id="6e0ab-109">Por exemplo, um conjunto esparso de descritores poderia ser copiado para um destino contíguo, vice-versa ou em alguma combinação.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-109">For example, a sparse set of descriptors could be copied to a contiguous destination, vice versa, or in some combination.</span></span>

<span data-ttu-id="6e0ab-110">Vários heaps de descritores podem ser envolvidos na operação de cópia, tanto como origem quanto destino.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-110">Multiple descriptor heaps can be involved in the copy operation, both as source and destination.</span></span> <span data-ttu-id="6e0ab-111">O uso de identificadores de descritor como parâmetros significa que os métodos de cópia não se preocupam com quais heaps um determinado descritor está. eles são apenas a memória.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-111">The use of descriptor handles as parameters means the copy methods don’t care about which heaps any given descriptor lies in – they are all just memory.</span></span>

<span data-ttu-id="6e0ab-112">Os tipos de heap de descritores sendo copiados de e para devem corresponder, portanto, os métodos usam um único tipo de heap de descritor como entrada.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-112">The descriptor heap types being copied from and to must match, so the methods take a single descriptor heap type as input.</span></span> <span data-ttu-id="6e0ab-113">O driver precisa saber o tipo de heap de todos os descritores na operação de cópia fornecida, portanto, ele sabe qual é o tamanho dos dados envolvidos na operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-113">The driver needs to know the heap type of all the descriptors in the given copy operation, so it knows what size of data is involved in the copy operation.</span></span> <span data-ttu-id="6e0ab-114">O driver também pode precisar fazer o trabalho de cópia personalizada se um determinado tipo de heap de descritor o garantir – um detalhe de implementação.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-114">The driver might also need to do custom copying work if a given descriptor heap type warrants it – an implementation detail.</span></span> <span data-ttu-id="6e0ab-115">Observe que os próprios identificadores de descritor não identificam de que tipo eles estão apontando; Portanto, um parâmetro adicional é necessário para a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-115">Note that descriptor handles themselves do not otherwise identify what type they are pointing to; therefore, an additional parameter is required for the copy operation.</span></span>

<span data-ttu-id="6e0ab-116">Uma API alternativa para [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) é fornecida para o caso simples de copiar um único intervalo de descritores de um local para outro – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span><span class="sxs-lookup"><span data-stu-id="6e0ab-116">An alternative API to [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) is provided for the simple case of copying a single range of descriptors from one location to another – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).</span></span>

<span data-ttu-id="6e0ab-117">Para esses métodos de cópia do descritor baseados em dispositivo (linha do tempo de CPU), os descritores de origem devem vir de um heap de descritor visível sem sombreador.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-117">For these device based (CPU timeline) descriptor copy methods, source descriptors must come from a non-shader visible descriptor heap.</span></span> <span data-ttu-id="6e0ab-118">Os descritores de destino podem estar em qualquer heap de descrição visível da CPU (sombreador visível ou não).</span><span class="sxs-lookup"><span data-stu-id="6e0ab-118">The destination descriptors can be in any descriptor heap that is CPU visible (shader visible or not).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e0ab-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e0ab-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ab-120">Descritores</span><span class="sxs-lookup"><span data-stu-id="6e0ab-120">Descriptors</span></span>](descriptors.md)
</dt> </dl>

 

 




