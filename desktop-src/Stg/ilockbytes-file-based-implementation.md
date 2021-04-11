---
title: ILockBytes-implementação de File-Based
description: Implementado em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e criado para leitura e gravação diretamente em um arquivo de disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implementações, com base em arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363747"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="838be-104">ILockBytes-implementação de File-Based</span><span class="sxs-lookup"><span data-stu-id="838be-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="838be-105">Implementado em um objeto de matriz de bytes subjacente a um objeto de armazenamento de arquivo composto COM e criado para leitura e gravação diretamente em um arquivo de disco.</span><span class="sxs-lookup"><span data-stu-id="838be-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="838be-106">Quando usar</span><span class="sxs-lookup"><span data-stu-id="838be-106">When to Use</span></span>

<span data-ttu-id="838be-107">Os métodos de [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) são chamados das implementações de arquivo composto de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) no objeto de armazenamento de arquivo composto criado por meio de uma chamada para [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), portanto, você não precisa chamá-los diretamente.</span><span class="sxs-lookup"><span data-stu-id="838be-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="838be-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="838be-108">Remarks</span></span>

<span data-ttu-id="838be-109">A seguir estão os métodos da implementação de File-Based do [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="838be-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="838be-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**</span><span class="sxs-lookup"><span data-stu-id="838be-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="838be-111">Lê um bloco de bytes de um deslocamento especificado no início da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="838be-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="838be-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="838be-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="838be-113">Grava um bloco de bytes de um deslocamento especificado no início da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="838be-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="838be-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: flush**</span><span class="sxs-lookup"><span data-stu-id="838be-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="838be-115">Garante que todos os buffers internos mantidos pela implementação do [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) sejam gravados no armazenamento físico subjacente.</span><span class="sxs-lookup"><span data-stu-id="838be-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="838be-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="838be-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="838be-117">Define o tamanho da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="838be-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="838be-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="838be-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="838be-119">O parâmetro *dwLockTypes* é definido para bloquear \_ ONLYONCE ou bloqueio \_ exclusivo, o que permitirá ou restringirá o acesso a regiões bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="838be-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="838be-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="838be-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="838be-121">Esse método desbloqueia a região bloqueada por [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span><span class="sxs-lookup"><span data-stu-id="838be-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="838be-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="838be-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="838be-123">A implementação de [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornecida pelo com chama o método [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) para recuperar informações sobre o objeto da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="838be-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="838be-124">Se não houver nenhum nome razoável para a matriz de bytes, o método **ILockBytes:: stat** fornecido com retornará **NULL** no membro **pwcsName** da estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="838be-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="838be-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="838be-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="838be-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="838be-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="838be-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="838be-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="838be-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="838be-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




