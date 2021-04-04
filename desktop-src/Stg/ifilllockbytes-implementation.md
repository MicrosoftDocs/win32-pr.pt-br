---
title: IFillLockBytes-implementação
description: O sistema fornece uma implementação de IFillLockBytes como parte da implementação dos arquivos compostos.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implementação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916241"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="27eeb-104">IFillLockBytes-implementação</span><span class="sxs-lookup"><span data-stu-id="27eeb-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="27eeb-105">O sistema fornece uma implementação de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) como parte da implementação dos arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="27eeb-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="27eeb-106">O download do código pode criar uma instância de um objeto de arquivo composto assíncrono chamando [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span><span class="sxs-lookup"><span data-stu-id="27eeb-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="27eeb-107">O download do código também pode criar uma instância de um objeto wrapper de matriz de bytes assíncronos em um arquivo ou matriz de bytes existente chamando a função [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) ou a função [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="27eeb-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="27eeb-108">Quando usar</span><span class="sxs-lookup"><span data-stu-id="27eeb-108">When to Use</span></span>

<span data-ttu-id="27eeb-109">Atualmente, os monikers de URL são os únicos usuários da implementação de armazenamento assíncrono COM.</span><span class="sxs-lookup"><span data-stu-id="27eeb-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="27eeb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="27eeb-110">Remarks</span></span>

<span data-ttu-id="27eeb-111">A seguir estão os quatro métodos da implementação de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .</span><span class="sxs-lookup"><span data-stu-id="27eeb-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="27eeb-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span><span class="sxs-lookup"><span data-stu-id="27eeb-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="27eeb-113">Grava um novo bloco de bytes no final de uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="27eeb-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="27eeb-114">O tamanho do bloco é especificado como um parâmetro para [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span><span class="sxs-lookup"><span data-stu-id="27eeb-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="27eeb-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span><span class="sxs-lookup"><span data-stu-id="27eeb-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="27eeb-116">Grava um novo bloco de dados em um local especificado na matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="27eeb-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="27eeb-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes:: preenche**</span><span class="sxs-lookup"><span data-stu-id="27eeb-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="27eeb-118">Define o tamanho da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="27eeb-118">Sets the size of the byte array.</span></span> <span data-ttu-id="27eeb-119">Retorna E \_ falha de chamadas para [**ILockBytes:: ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) que tentam acessar dados além do limite superior especificado pelo método.</span><span class="sxs-lookup"><span data-stu-id="27eeb-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="27eeb-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes:: Terminate**</span><span class="sxs-lookup"><span data-stu-id="27eeb-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="27eeb-121">Informa a matriz de bytes que um download foi encerrado, com êxito ou sem êxito.</span><span class="sxs-lookup"><span data-stu-id="27eeb-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




