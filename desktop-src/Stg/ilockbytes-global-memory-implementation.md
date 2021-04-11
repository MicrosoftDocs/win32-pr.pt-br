---
title: ILockBytes-implementação de memória global
description: A implementação de memória global ILockBytes é implementada em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e projetada para leitura e gravação diretamente na memória global.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implementações, memória global
- ILockBytes Strctd STG, implementações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291905"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="c53d1-105">ILockBytes-implementação de memória global</span><span class="sxs-lookup"><span data-stu-id="c53d1-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="c53d1-106">A implementação de memória global ILockBytes é implementada em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e projetada para leitura e gravação diretamente na memória global.</span><span class="sxs-lookup"><span data-stu-id="c53d1-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c53d1-107">Quando usar</span><span class="sxs-lookup"><span data-stu-id="c53d1-107">When to Use</span></span>

<span data-ttu-id="c53d1-108">Os métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) são chamados das implementações de arquivo composto de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no objeto de armazenamento de arquivo composto criado por meio de uma chamada para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span><span class="sxs-lookup"><span data-stu-id="c53d1-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="c53d1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c53d1-109">Remarks</span></span>

<span data-ttu-id="c53d1-110">A seguir estão os métodos da implementação de memória global [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="c53d1-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="c53d1-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**</span><span class="sxs-lookup"><span data-stu-id="c53d1-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-112">Lê um bloco de bytes de um deslocamento especificado no início da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c53d1-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="c53d1-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-114">Grava o bloco de bytes de um deslocamento especificado no início da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c53d1-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: flush**</span><span class="sxs-lookup"><span data-stu-id="c53d1-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-116">Diferentemente da implementação baseada em arquivo, chamar esse método na implementação de memória global não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="c53d1-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="c53d1-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-118">Define o tamanho da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c53d1-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="c53d1-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-120">Essa implementação não dá suporte ao bloqueio, portanto *dwLocksType* está definido como zero.</span><span class="sxs-lookup"><span data-stu-id="c53d1-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="c53d1-121">O chamador deve garantir que os acessos sejam válidos e mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c53d1-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="c53d1-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-123">Esta implementação não dá suporte a bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c53d1-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="c53d1-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="c53d1-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="c53d1-125">A implementação de [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornecida pelo com chama o método [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar dados sobre o objeto da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="c53d1-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="c53d1-126">Se não houver nenhum nome razoável para a matriz de bytes, o método **ILockBytes:: stat** fornecido com retornará **NULL** no membro **pwcsName** da estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="c53d1-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c53d1-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c53d1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c53d1-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="c53d1-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="c53d1-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="c53d1-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="c53d1-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="c53d1-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




