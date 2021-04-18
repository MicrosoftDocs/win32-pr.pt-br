---
title: IStream-implementação de arquivo composto
description: A interface IStream dá suporte à leitura e gravação de dados em objetos de fluxo. Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- Strctd de IStream STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105756538"
---
# <a name="istream---compound-file-implementation"></a><span data-ttu-id="f7a93-105">IStream-implementação de arquivo composto</span><span class="sxs-lookup"><span data-stu-id="f7a93-105">IStream - Compound File Implementation</span></span>

<span data-ttu-id="f7a93-106">A interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dá suporte à leitura e gravação de dados em objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-106">The [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface supports reading and writing data to stream objects.</span></span> <span data-ttu-id="f7a93-107">Em um objeto de armazenamento estruturado, os objetos de fluxo contêm os dados e os armazenamentos fornecem a estrutura.</span><span class="sxs-lookup"><span data-stu-id="f7a93-107">In a structured storage object, stream objects contain the data and storages provide the structure.</span></span> <span data-ttu-id="f7a93-108">Dados simples podem ser gravados diretamente em um fluxo, mas com mais frequência, os fluxos são elementos aninhados em um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f7a93-108">Simple data can be written directly to a stream, but more frequently, streams are elements nested within a storage object.</span></span> <span data-ttu-id="f7a93-109">Eles são semelhantes aos arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="f7a93-109">They are similar to standard files.</span></span>

<span data-ttu-id="f7a93-110">A especificação de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) define mais funcionalidade do que a implementação com dá suporte a.</span><span class="sxs-lookup"><span data-stu-id="f7a93-110">The specification of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) defines more functionality than the COM implementation supports.</span></span> <span data-ttu-id="f7a93-111">Por exemplo, a interface **IStream** define fluxos de até 2 ⁶ ⁴ bytes de comprimento que exigem um ponteiro de busca de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f7a93-111">For example, the **IStream** interface defines streams up to 2⁶⁴ bytes in length requiring a 64-bit seek pointer.</span></span> <span data-ttu-id="f7a93-112">No entanto, a implementação COM só dá suporte a fluxos de até 2 ³ ² bytes de comprimento (4 GB) e as operações de leitura e gravação são sempre limitadas a 2 ³ ² bytes por vez.</span><span class="sxs-lookup"><span data-stu-id="f7a93-112">However, the COM implementation only supports streams up to 2³² bytes in length (4 GB) and read and write operations are always limited to 2³² bytes at a time.</span></span> <span data-ttu-id="f7a93-113">A implementação COM também não oferece suporte a transacionamento de fluxo ou bloqueio de região.</span><span class="sxs-lookup"><span data-stu-id="f7a93-113">The COM implementation also does not support stream transactioning or region locking.</span></span>

<span data-ttu-id="f7a93-114">Para criar um fluxo simples baseado na memória global, obtenha um ponteiro de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chamando a função de API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span><span class="sxs-lookup"><span data-stu-id="f7a93-114">To create a simple stream based on global memory, get an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer by calling the API function [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal).</span></span> <span data-ttu-id="f7a93-115">Para obter um ponteiro de **IStream** em um objeto de arquivo composto, chame [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span><span class="sxs-lookup"><span data-stu-id="f7a93-115">To get an **IStream** pointer within a compound file object, call either [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) or [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage).</span></span> <span data-ttu-id="f7a93-116">Essas funções recuperam um ponteiro [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , com o qual você pode chamar [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) para um ponteiro de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="f7a93-116">These functions retrieve an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer, with which you can then call [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) or [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) for an **IStream** pointer.</span></span> <span data-ttu-id="f7a93-117">Em ambos os casos, o mesmo código de implementação de **IStream** é usado.</span><span class="sxs-lookup"><span data-stu-id="f7a93-117">In either case, the same **IStream** implementation code is used.</span></span>

> [!Note]  
> <span data-ttu-id="f7a93-118">A implementação do arquivo composto do armazenamento estruturado não tem sucesso em um método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), mas inclui os métodos de [**leitura**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) e [**gravação**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) por meio do ponteiro de interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="f7a93-118">The compound file implementation of structured storage does not succeed on a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method for [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), but it includes the [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) and [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) methods through the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer.</span></span>

 

## <a name="when-to-use"></a><span data-ttu-id="f7a93-119">Quando usar</span><span class="sxs-lookup"><span data-stu-id="f7a93-119">When to Use</span></span>

<span data-ttu-id="f7a93-120">Chame os métodos de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para ler e gravar dados em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-120">Call the methods of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) to read and write data to a stream.</span></span>

<span data-ttu-id="f7a93-121">Como os objetos de fluxo podem ser empacotados para outros processos, os aplicativos podem compartilhar os dados em objetos de armazenamento sem precisar usar memória global.</span><span class="sxs-lookup"><span data-stu-id="f7a93-121">Because stream objects can be marshaled to other processes, applications can share the data in storage objects without having to use global memory.</span></span> <span data-ttu-id="f7a93-122">Na implementação de arquivo composto COM de objetos de fluxo, os recursos de marshaling personalizados em COM criam uma versão remota do objeto original no novo processo quando os dois processos têm acesso compartilhado à memória.</span><span class="sxs-lookup"><span data-stu-id="f7a93-122">In the COM compound file implementation of stream objects, the custom marshaling facilities in COM create a remote version of the original object in the new process when the two processes have shared-memory access.</span></span> <span data-ttu-id="f7a93-123">Portanto, a versão remota não precisa se comunicar com o processo original para realizar suas funções.</span><span class="sxs-lookup"><span data-stu-id="f7a93-123">Thus, the remote version does not need to communicate with the original process to carry out its functions.</span></span>

<span data-ttu-id="f7a93-124">A versão remota do objeto de fluxo compartilha o mesmo ponteiro de busca que o fluxo original.</span><span class="sxs-lookup"><span data-stu-id="f7a93-124">The remote version of the stream object shares the same seek pointer as the original stream.</span></span> <span data-ttu-id="f7a93-125">Se você não quiser compartilhar o ponteiro de busca, use o método [**IStream:: clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) para fornecer uma cópia do objeto de fluxo para o processo remoto.</span><span class="sxs-lookup"><span data-stu-id="f7a93-125">If you do not want to share the seek pointer, use the [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) method to provide a copy of the stream object for the remote process.</span></span>

> [!Note]
> <span data-ttu-id="f7a93-126">Se você estiver criando um objeto de fluxo maior do que o heap na memória do computador e estiver usando um identificador **HGLOBAL** para um objeto de memória global, o objeto de fluxo chamará o método [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente quando ele exigir mais memória.</span><span class="sxs-lookup"><span data-stu-id="f7a93-126">If creating a stream object that is larger than the heap in your computer's memory and you are using an **HGLOBAL** handle to a global memory object, the stream object calls the [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) method internally whe it requires more memory.</span></span> <span data-ttu-id="f7a93-127">Como o **GlobalRealloc** sempre copia dados da origem para o destino, o aumento de um objeto de fluxo de 20 MB para 25 MB, por exemplo, requer grandes quantidades de tempo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-127">Because **GlobalRealloc** always copies data from the source to the destination, increasing a stream object from 20 MB to 25 MB, for example, requires large amounts of time.</span></span> <span data-ttu-id="f7a93-128">Isso ocorre devido ao tamanho dos incrementos copiados e é worsened se houver menos de 45 MB de memória no computador devido à troca de disco.</span><span class="sxs-lookup"><span data-stu-id="f7a93-128">This is due to the size of the increments copied and is worsened if there is less than 45 MB of memory on the computer because of disk swapping.</span></span>
>
> <span data-ttu-id="f7a93-129">A solução preferida é implementar um método [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que usa a memória alocada pelo [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) em vez de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span><span class="sxs-lookup"><span data-stu-id="f7a93-129">The preferred solution is to implement an [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) method that uses memory allocated by [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) instead of [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc).</span></span> <span data-ttu-id="f7a93-130">Isso pode reservar uma grande parte do espaço de endereço virtual e, em seguida, confirmar a memória dentro desse espaço de endereço conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f7a93-130">This can reserve a large chunk of virtual address space and then commit memory within that address space as required.</span></span> <span data-ttu-id="f7a93-131">Nenhuma cópia de dados ocorre e a memória é confirmada apenas conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f7a93-131">No data copying occurs and memory is committed only as it is required.</span></span>
>
> <span data-ttu-id="f7a93-132">Uma alternativa para [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) é chamar o método [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) no objeto Stream para aumentar a alocação de memória com antecedência.</span><span class="sxs-lookup"><span data-stu-id="f7a93-132">An alternative to [**GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) is to call the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method on the stream object to increase the memory allocation in advance.</span></span> <span data-ttu-id="f7a93-133">No entanto, isso não é tão eficiente quanto usar o [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="f7a93-133">This is not, however, as efficient as using [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), as described above.</span></span>

 

## <a name="methods"></a><span data-ttu-id="f7a93-134">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7a93-134">Methods</span></span>

<dl> <dt>

<span data-ttu-id="f7a93-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: ler**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span><span class="sxs-lookup"><span data-stu-id="f7a93-135"><span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-136">Lê um número especificado de bytes do objeto de fluxo para a memória, a partir do ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="f7a93-136">Reads a specified number of bytes from the stream object into memory starting at the current seek pointer.</span></span> <span data-ttu-id="f7a93-137">Essa implementação retornará S \_ OK se o final do fluxo for atingido durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="f7a93-137">This implementation returns S\_OK if the end of the stream was reached during the read.</span></span> <span data-ttu-id="f7a93-138">(Isso é o mesmo que o comportamento "fim do arquivo" encontrado no sistema de arquivos FAT do MS-DOS.)</span><span class="sxs-lookup"><span data-stu-id="f7a93-138">(This is the same as the "end of file" behavior found in the MS-DOS FAT file system.)</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span><span class="sxs-lookup"><span data-stu-id="f7a93-139"><span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-140">Grava um número especificado de bytes no objeto de fluxo a partir do ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="f7a93-140">Writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span> <span data-ttu-id="f7a93-141">Nessa implementação, os objetos de fluxo não são esparsos.</span><span class="sxs-lookup"><span data-stu-id="f7a93-141">In this implementation, stream objects are not sparse.</span></span> <span data-ttu-id="f7a93-142">Todos os bytes de preenchimento são eventualmente alocados no disco e atribuídos ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-142">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span><span class="sxs-lookup"><span data-stu-id="f7a93-143"><span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-144">Altera o ponteiro de busca para um novo local relativo ao início do fluxo, ao fim do fluxo ou ao ponteiro de busca atual.</span><span class="sxs-lookup"><span data-stu-id="f7a93-144">Changes the seek pointer to a new location relative to the beginning of the stream, to the end of the stream, or to the current seek pointer.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span><span class="sxs-lookup"><span data-stu-id="f7a93-145"><span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-146">Altera o tamanho do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-146">Changes the size of the stream object.</span></span> <span data-ttu-id="f7a93-147">Nessa implementação, não há nenhuma garantia de que o espaço alocado será contíguo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-147">In this implementation, there is no guarantee that the space allocated will be contiguous.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span><span class="sxs-lookup"><span data-stu-id="f7a93-148"><span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-149">Copia um número especificado de bytes do ponteiro de busca atual no fluxo para o ponteiro de busca atual em outro fluxo.</span><span class="sxs-lookup"><span data-stu-id="f7a93-149">Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span><span class="sxs-lookup"><span data-stu-id="f7a93-150"><span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-151">A implementação do arquivo composto de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) dá suporte à abertura de fluxos somente no modo direto, não no modo transacionado.</span><span class="sxs-lookup"><span data-stu-id="f7a93-151">The compound file implementation of [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supports opening streams only in direct mode, not transacted mode.</span></span> <span data-ttu-id="f7a93-152">Portanto, o método não tem nenhum efeito quando chamado que não libera todos os buffers de memória para o próximo nível de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f7a93-152">Therefore, the method has no effect when called other than to flush all memory buffers to the next storage level.</span></span>

<span data-ttu-id="f7a93-153">Nessa implementação, não importa se você confirma as alterações em fluxos, só precisa confirmar as alterações para objetos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f7a93-153">In this implementation, it does not matter if you commit changes to streams, you need only commit changes for storage objects.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span><span class="sxs-lookup"><span data-stu-id="f7a93-154"><span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-155">Essa implementação não dá suporte a fluxos transacionados, portanto, uma chamada para esse método não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="f7a93-155">This implementation does not support transacted streams, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span><span class="sxs-lookup"><span data-stu-id="f7a93-156"><span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-157">O bloqueio de intervalo não tem suporte nesta implementação, portanto, uma chamada para esse método não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="f7a93-157">Range-locking is not supported by this implementation, so a call to this method has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span><span class="sxs-lookup"><span data-stu-id="f7a93-158"><span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-159">Remove a restrição de acesso em um intervalo de bytes anteriormente restritos com [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span><span class="sxs-lookup"><span data-stu-id="f7a93-159">Removes the access restriction on a range of bytes previously restricted with [**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span><span class="sxs-lookup"><span data-stu-id="f7a93-160"><span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-161">Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este fluxo</span><span class="sxs-lookup"><span data-stu-id="f7a93-161">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this stream</span></span>

</dd> <dt>

<span data-ttu-id="f7a93-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span><span class="sxs-lookup"><span data-stu-id="f7a93-162"><span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)</span></span>
</dt> <dd>

<span data-ttu-id="f7a93-163">Cria um novo objeto de fluxo com seu próprio ponteiro de busca que referencia os mesmos bytes como o fluxo original.</span><span class="sxs-lookup"><span data-stu-id="f7a93-163">Creates a new stream object with its own seek pointer that references the same bytes as the original stream.</span></span>

</dd> </dl>

<span data-ttu-id="f7a93-164">Um [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) de modo simples está sujeito às restrições a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7a93-164">A simple-mode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is subject to the following constraints.</span></span>

-   <span data-ttu-id="f7a93-165">Um fluxo é modo simples se foi criado ou aberto a partir de um armazenamento de modo simples.</span><span class="sxs-lookup"><span data-stu-id="f7a93-165">A stream is simple mode if it was created or opened from a simple-mode storage.</span></span> <span data-ttu-id="f7a93-166">Um armazenamento será modo simples se for criado ou aberto com o \_ sinalizador simples STGM definido no parâmetro *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="f7a93-166">A storage is simple mode if it is created or opened with the STGM\_SIMPLE flag set in the *grfMode* parameter.</span></span>
-   <span data-ttu-id="f7a93-167">Não há suporte para os métodos [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) e [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) .</span><span class="sxs-lookup"><span data-stu-id="f7a93-167">The [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) and [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) methods are not supported.</span></span>
-   <span data-ttu-id="f7a93-168">Há suporte para o método [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , mas o \_ valor NoName de STATFLAG deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="f7a93-168">The [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method is supported, but the STATFLAG\_NONAME value must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7a93-169">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7a93-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a93-170">**IStream**</span><span class="sxs-lookup"><span data-stu-id="f7a93-170">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="f7a93-171">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="f7a93-171">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="f7a93-172">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="f7a93-172">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[<span data-ttu-id="f7a93-173">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="f7a93-173">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="f7a93-174">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="f7a93-174">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 