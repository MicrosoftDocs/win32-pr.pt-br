---
title: Constantes STGM (ObjBase. h)
description: Sinalizadores que indicam as condições para criar e excluir o objeto e os modos de acesso do objeto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454734"
---
# <a name="stgm-constants"></a><span data-ttu-id="2dfec-103">Constantes STGM</span><span class="sxs-lookup"><span data-stu-id="2dfec-103">STGM Constants</span></span>

<span data-ttu-id="2dfec-104">As constantes STGM são sinalizadores que indicam as condições para criar e excluir o objeto e os modos de acesso para o objeto.</span><span class="sxs-lookup"><span data-stu-id="2dfec-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="2dfec-105">As constantes STGM estão incluídas nas interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e nas funções [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="2dfec-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="2dfec-106">Esses elementos geralmente são combinados usando um operador **or**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="2dfec-107">Eles são interpretados em grupos, conforme listado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2dfec-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="2dfec-108">Não é válido usar mais de um elemento de um único grupo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="2dfec-109">Use um sinalizador do grupo de criação ao criar um objeto, como com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="2dfec-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="2dfec-110">Para obter mais informações sobre transacionamento, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="2dfec-111">Agrupar</span><span class="sxs-lookup"><span data-stu-id="2dfec-111">Group</span></span>                      | <span data-ttu-id="2dfec-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="2dfec-112">Flag</span></span>                         | <span data-ttu-id="2dfec-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2dfec-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="2dfec-114">Access</span><span class="sxs-lookup"><span data-stu-id="2dfec-114">Access</span></span>                     | <span data-ttu-id="2dfec-115">**STGM \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="2dfec-115">**STGM\_READ**</span></span>               | <span data-ttu-id="2dfec-116">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="2dfec-117">**STGM \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="2dfec-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="2dfec-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="2dfec-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="2dfec-119">**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="2dfec-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="2dfec-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="2dfec-120">0x00000002L</span></span> |
| <span data-ttu-id="2dfec-121">Compartilhamento</span><span class="sxs-lookup"><span data-stu-id="2dfec-121">Sharing</span></span>                    | <span data-ttu-id="2dfec-122">**\_negação de compartilhamento de STGM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2dfec-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="2dfec-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="2dfec-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="2dfec-124">**\_leitura de \_ negação de compartilhamento de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfec-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="2dfec-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="2dfec-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="2dfec-126">**STGM \_ compartilhamento \_ negar \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="2dfec-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="2dfec-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="2dfec-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="2dfec-128">**STGM de \_ compartilhamento \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="2dfec-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="2dfec-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="2dfec-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="2dfec-130">**\_prioridade STGM**</span><span class="sxs-lookup"><span data-stu-id="2dfec-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="2dfec-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-131">0x00040000L</span></span> |
| <span data-ttu-id="2dfec-132">Criação</span><span class="sxs-lookup"><span data-stu-id="2dfec-132">Creation</span></span>                   | <span data-ttu-id="2dfec-133">**STGM \_ criar**</span><span class="sxs-lookup"><span data-stu-id="2dfec-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="2dfec-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="2dfec-135">**STGM \_ converter**</span><span class="sxs-lookup"><span data-stu-id="2dfec-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="2dfec-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="2dfec-137">**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="2dfec-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="2dfec-138">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-138">0x00000000L</span></span> |
| <span data-ttu-id="2dfec-139">Transacionando</span><span class="sxs-lookup"><span data-stu-id="2dfec-139">Transactioning</span></span>             | <span data-ttu-id="2dfec-140">**STGM \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="2dfec-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="2dfec-141">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="2dfec-142">**STGM \_ transacionado**</span><span class="sxs-lookup"><span data-stu-id="2dfec-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="2dfec-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-143">0x00010000L</span></span> |
| <span data-ttu-id="2dfec-144">Desempenho de transação</span><span class="sxs-lookup"><span data-stu-id="2dfec-144">Transactioning Performance</span></span> | <span data-ttu-id="2dfec-145">**STGM do \_ zero**</span><span class="sxs-lookup"><span data-stu-id="2dfec-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="2dfec-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="2dfec-147">**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="2dfec-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="2dfec-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-148">0x00200000L</span></span> |
| <span data-ttu-id="2dfec-149">Direto SWMR e simples</span><span class="sxs-lookup"><span data-stu-id="2dfec-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="2dfec-150">**STGM \_ simples**</span><span class="sxs-lookup"><span data-stu-id="2dfec-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="2dfec-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="2dfec-152">**STGM \_ direto \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="2dfec-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="2dfec-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-153">0x00400000L</span></span> |
| <span data-ttu-id="2dfec-154">Excluir na versão</span><span class="sxs-lookup"><span data-stu-id="2dfec-154">Delete On Release</span></span>          | <span data-ttu-id="2dfec-155">**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="2dfec-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="2dfec-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="2dfec-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="2dfec-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-158">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-159">Indica que o objeto é somente leitura, o que significa que não é possível fazer modificações.</span><span class="sxs-lookup"><span data-stu-id="2dfec-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="2dfec-160">Por exemplo, se um objeto Stream for aberto com **STGM \_ Read**, o método [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) poderá ser chamado, mas o método [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) poderá não.</span><span class="sxs-lookup"><span data-stu-id="2dfec-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="2dfec-161">Da mesma forma, se um objeto de armazenamento aberto com **STGM \_ Read**, os métodos [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) e [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) podem ser chamados, mas os métodos [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) podem não.</span><span class="sxs-lookup"><span data-stu-id="2dfec-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="2dfec-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="2dfec-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-164">Permite salvar alterações no objeto, mas não permite o acesso a seus dados.</span><span class="sxs-lookup"><span data-stu-id="2dfec-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="2dfec-165">As implementações fornecidas das interfaces [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) não dão suporte a esse modo somente gravação.</span><span class="sxs-lookup"><span data-stu-id="2dfec-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ ReadWrite**</span><span class="sxs-lookup"><span data-stu-id="2dfec-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="2dfec-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-168">Habilita o acesso e a modificação de dados de objeto.</span><span class="sxs-lookup"><span data-stu-id="2dfec-168">Enables access and modification of object data.</span></span> <span data-ttu-id="2dfec-169">Por exemplo, se um objeto de fluxo for criado ou aberto nesse modo, será possível chamar ambos os [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStream:: Write**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="2dfec-170">Lembre-se de que essa constante não é um binário simples **ou** uma operação dos elementos **STGM \_ Write** e **STGM \_ Read** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**\_negação de compartilhamento de STGM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2dfec-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="2dfec-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-173">Especifica que aberturas subsequentes do objeto não têm acesso de leitura ou gravação negado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="2dfec-174">Se nenhum sinalizador do grupo de compartilhamento for especificado, esse sinalizador será assumido.</span><span class="sxs-lookup"><span data-stu-id="2dfec-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**\_leitura de \_ negação de compartilhamento de STGM \_**</span><span class="sxs-lookup"><span data-stu-id="2dfec-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="2dfec-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-177">Impede que outras pessoas abram subsequentemente o objeto no modo de **\_ leitura STGM** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="2dfec-178">Normalmente, ele é usado em um objeto de armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="2dfec-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ compartilhamento \_ negar \_ gravação**</span><span class="sxs-lookup"><span data-stu-id="2dfec-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="2dfec-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-181">Impede que outras pessoas abram subsequentemente o objeto para acesso **STGM \_ Write** ou **STGM \_ ReadWrite** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="2dfec-182">No modo transacionado, o compartilhamento de **\_ \_ \_ gravação de negação de compartilhamento STGM** ou **STGM \_ \_ exclusivo** pode melhorar significativamente o desempenho porque eles não exigem instantâneos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="2dfec-183">Para obter mais informações sobre transacionamento, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM de \_ compartilhamento \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="2dfec-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="2dfec-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-186">Impede que outras pessoas abram posteriormente o objeto em qualquer modo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="2dfec-187">Lembre-se de que esse valor não é uma operação unificada **ou** simples dos valores de **\_ negação STGM compartilhamento de \_ \_ leitura** e **\_ \_ negação \_** do compartilhamento de STGM.</span><span class="sxs-lookup"><span data-stu-id="2dfec-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="2dfec-188">No modo transacionado, o compartilhamento de **\_ \_ \_ gravação de negação de compartilhamento STGM** ou **STGM \_ \_ exclusivo** pode melhorar significativamente o desempenho porque eles não exigem instantâneos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="2dfec-189">Para obter mais informações sobre transacionamento, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_prioridade STGM**</span><span class="sxs-lookup"><span data-stu-id="2dfec-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-192">Abre o objeto de armazenamento com acesso exclusivo à versão confirmada mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="2dfec-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="2dfec-193">Portanto, outros usuários não podem confirmar alterações no objeto enquanto você o abre no modo de prioridade.</span><span class="sxs-lookup"><span data-stu-id="2dfec-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="2dfec-194">Você tem benefícios de desempenho para operações de cópia, mas impede que outras pessoas confirmassem alterações.</span><span class="sxs-lookup"><span data-stu-id="2dfec-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="2dfec-195">Limite o tempo em que os objetos são abertos no modo de prioridade.</span><span class="sxs-lookup"><span data-stu-id="2dfec-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="2dfec-196">Você deve especificar **STGM \_ Direct** e **STGM \_ Read** com o modo Priority e não pode especificar **STGM \_ DELETEONRELEASE**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="2dfec-197">**STGM \_ DELETEONRELEASE** é válido somente ao criar um objeto raiz, como com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="2dfec-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="2dfec-198">Ele não é válido ao abrir um objeto raiz existente, como com [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="2dfec-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="2dfec-199">Ele também não é válido ao criar ou abrir um subelemento, como com [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span><span class="sxs-lookup"><span data-stu-id="2dfec-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ criar**</span><span class="sxs-lookup"><span data-stu-id="2dfec-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-202">Indica que um fluxo ou objeto de armazenamento existente deve ser removido antes que o novo objeto o substitua.</span><span class="sxs-lookup"><span data-stu-id="2dfec-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="2dfec-203">Um novo objeto será criado quando esse sinalizador for especificado somente se o objeto existente tiver sido removido com êxito.</span><span class="sxs-lookup"><span data-stu-id="2dfec-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="2dfec-204">Esse sinalizador é usado ao tentar criar:</span><span class="sxs-lookup"><span data-stu-id="2dfec-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="2dfec-205">Um objeto de armazenamento em um disco, mas existe um arquivo com esse nome.</span><span class="sxs-lookup"><span data-stu-id="2dfec-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="2dfec-206">Um objeto dentro de um objeto de armazenamento, mas existe um objeto com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="2dfec-207">Um objeto de matriz de bytes, mas existe um com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="2dfec-208">Esse sinalizador não pode ser usado com operações abertas, como [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ou [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="2dfec-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ converter**</span><span class="sxs-lookup"><span data-stu-id="2dfec-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-211">Cria o novo objeto enquanto preserva os dados existentes em um fluxo denominado "conteúdo".</span><span class="sxs-lookup"><span data-stu-id="2dfec-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="2dfec-212">No caso de um objeto de armazenamento ou de uma matriz de bytes, os dados antigos são formatados em um fluxo, independentemente de o arquivo ou a matriz de bytes existente atualmente conter um objeto de armazenamento em camadas.</span><span class="sxs-lookup"><span data-stu-id="2dfec-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="2dfec-213">Esse sinalizador só pode ser usado ao criar um objeto de armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="2dfec-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="2dfec-214">Ele não pode ser usado em um objeto de armazenamento; por exemplo, em [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="2dfec-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="2dfec-215">Também não é válido usar esse sinalizador e o sinalizador **STGM \_ DELETEONRELEASE** simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2dfec-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAILIFTHERE**</span><span class="sxs-lookup"><span data-stu-id="2dfec-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-217">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-218">Faz com que a operação de criação falhe se um objeto existente com o nome especificado existir.</span><span class="sxs-lookup"><span data-stu-id="2dfec-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="2dfec-219">Nesse caso, **STG \_ E \_ FILEALREADYEXISTS** são retornados.</span><span class="sxs-lookup"><span data-stu-id="2dfec-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="2dfec-220">Este é o modo de criação padrão; ou seja, se nenhum outro sinalizador de criação for especificado, **STGM \_ FAILIFTHERE** será implícito.</span><span class="sxs-lookup"><span data-stu-id="2dfec-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="2dfec-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-222">0x00000000l</span><span class="sxs-lookup"><span data-stu-id="2dfec-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-223">Indica que, no modo direto, cada alteração em um elemento de armazenamento ou de fluxo é gravada como ocorre.</span><span class="sxs-lookup"><span data-stu-id="2dfec-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="2dfec-224">Esse será o padrão se nem **STGM \_ Direct** nem **STGM \_ transacionado** for especificado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transacionado**</span><span class="sxs-lookup"><span data-stu-id="2dfec-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-227">Indica que, no modo transacionado, as alterações serão armazenadas em buffer e gravadas somente se uma operação de confirmação explícita for chamada.</span><span class="sxs-lookup"><span data-stu-id="2dfec-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="2dfec-228">Para ignorar as alterações, chame o método [**REVERT**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) na interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)ou [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .</span><span class="sxs-lookup"><span data-stu-id="2dfec-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="2dfec-229">A implementação do arquivo composto COM do **IStorage** não oferece suporte a fluxos transacionados, o que significa que os fluxos podem ser abertos somente no modo direto, e você não pode reverter alterações para eles, no entanto, há suporte para armazenamentos transacionados.</span><span class="sxs-lookup"><span data-stu-id="2dfec-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="2dfec-230">As implementações do sistema de arquivos composto, autônomo e NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) da mesma forma não dão suporte a conjuntos de propriedades transacionais e simples porque esses conjuntos de propriedades são armazenados em fluxos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="2dfec-231">No entanto, a transacção de conjuntos de propriedades não simples, que podem ser criados pela especificação do sinalizador **PROPSETFLAG não \_ simples** no parâmetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), tem suporte.</span><span class="sxs-lookup"><span data-stu-id="2dfec-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM do \_ zero**</span><span class="sxs-lookup"><span data-stu-id="2dfec-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-234">Indica que, no modo transacionado, um arquivo de rascunho temporário geralmente é usado para salvar as modificações até que o método **Commit** seja chamado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="2dfec-235">Especificar **STGM \_ noscratch** permite que a parte não utilizada do arquivo original seja usada como espaço de trabalho em vez de criar um novo arquivo para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="2dfec-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="2dfec-236">Isso não afeta os dados no arquivo original e, em determinados casos, pode resultar em um desempenho aprimorado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="2dfec-237">Não é válido especificar esse sinalizador sem especificar também **STGM \_ transacionado**, e esse sinalizador só pode ser usado em uma raiz aberta.</span><span class="sxs-lookup"><span data-stu-id="2dfec-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="2dfec-238">Para obter mais informações sobre o modo noscratch, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="2dfec-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-241">Esse sinalizador é usado ao abrir um objeto de armazenamento com **STGM \_ transacionado** e sem **STGM \_ compartilhamento \_ exclusivo** ou **STGM \_ compartilhamento \_ negar \_ gravação**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="2dfec-242">Nesse caso, especificar **STGM \_ nosnapshot** impede que a implementação fornecida pelo sistema crie uma cópia de instantâneo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="2dfec-243">Em vez disso, as alterações no arquivo são gravadas no final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="2dfec-244">O espaço não utilizado não é recuperado a menos que a consolidação seja executada durante a confirmação, e há apenas um gravador atual no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="2dfec-245">Quando o arquivo é aberto no modo sem instantâneo, não é possível executar outra operação aberta sem especificar **STGM \_ nosnapshot**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="2dfec-246">Esse sinalizador só pode ser usado em uma operação de abertura de raiz.</span><span class="sxs-lookup"><span data-stu-id="2dfec-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="2dfec-247">Para obter mais informações sobre o modo nosnapshot, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ simples**</span><span class="sxs-lookup"><span data-stu-id="2dfec-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-250">Fornece uma implementação mais rápida de um arquivo composto em um caso limitado, mas frequentemente usado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="2dfec-251">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ direto \_ SWMR**</span><span class="sxs-lookup"><span data-stu-id="2dfec-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-254">Dá suporte ao modo direto para operações de arquivo de gravador único e multileitura.</span><span class="sxs-lookup"><span data-stu-id="2dfec-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="2dfec-255">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2dfec-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**</span><span class="sxs-lookup"><span data-stu-id="2dfec-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2dfec-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="2dfec-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="2dfec-258">Indica que o arquivo subjacente deve ser destruído automaticamente quando o objeto de armazenamento raiz for liberado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="2dfec-259">Esse recurso é mais útil para a criação de arquivos temporários.</span><span class="sxs-lookup"><span data-stu-id="2dfec-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="2dfec-260">Esse sinalizador só pode ser usado ao criar um objeto raiz, como com [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="2dfec-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="2dfec-261">Ele não é válido ao abrir um objeto raiz, como with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), ou ao criar ou abrir um subelemento, como com [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="2dfec-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="2dfec-262">Também não é válido usar esse sinalizador e o \_ sinalizador STGM Convert simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2dfec-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dfec-263">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dfec-263">Remarks</span></span>

<span data-ttu-id="2dfec-264">Você pode combinar esses sinalizadores, mas só pode escolher um sinalizador de cada grupo de sinalizadores relacionados.</span><span class="sxs-lookup"><span data-stu-id="2dfec-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="2dfec-265">Normalmente, um sinalizador de cada um dos grupos de acesso e compartilhamento deve ser especificado para todas as funções e métodos que usam essas constantes.</span><span class="sxs-lookup"><span data-stu-id="2dfec-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="2dfec-266">Os sinalizadores de outros grupos são opcionais.</span><span class="sxs-lookup"><span data-stu-id="2dfec-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="2dfec-267">Modo transacionado</span><span class="sxs-lookup"><span data-stu-id="2dfec-267">Transacted Mode</span></span>

<span data-ttu-id="2dfec-268">Quando o **sinalizador \_ direto STGM** é especificado, somente uma das seguintes combinações de sinalizadores pode ser especificada nos grupos de acesso e compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2dfec-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="2dfec-269">Lembre-se de que o modo direto é implícito pela ausência de **STGM \_ transacionada**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="2dfec-270">Ou seja, se nem **STGM \_ Direct** nem **STGM \_ transacionado** for especificado, **STGM \_ Direct** será assumido.</span><span class="sxs-lookup"><span data-stu-id="2dfec-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="2dfec-271">Quando o **sinalizador \_ transacionado STGM** é especificado, os objetos são criados ou abertos no modo transacionado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="2dfec-272">Nesse modo, as alterações em um objeto não são mantidas até que sejam confirmadas.</span><span class="sxs-lookup"><span data-stu-id="2dfec-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="2dfec-273">Por exemplo, as alterações em um objeto de armazenamento transacionado não são mantidas até que o método [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="2dfec-274">As alterações nesse objeto de armazenamento serão perdidas se o objeto de armazenamento for liberado (versão final) antes de o método **Commit** ser chamado ou se o método [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) for chamado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="2dfec-275">Quando um objeto é criado ou aberto no modo transacionado, a implementação deve manter os dados originais e as atualizações para esses dados, para que as atualizações possam ser revertidas, se necessário.</span><span class="sxs-lookup"><span data-stu-id="2dfec-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="2dfec-276">Normalmente, isso é realizado por meio da gravação de alterações em uma área de rascunho até que elas sejam confirmadas ou pela criação de uma cópia, chamada de instantâneo, dos dados confirmados mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="2dfec-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="2dfec-277">Quando um objeto de armazenamento raiz é aberto no modo transacionado, o local e o comportamento dos dados de rascunho e das cópias de instantâneo podem ser controlados para otimizar o desempenho com os sinalizadores **NoSTGMnt \_ noscratch** e **STGM \_ nosnapshot** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="2dfec-278">(Um objeto de armazenamento raiz é obtido de, por exemplo, a função [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) ; um objeto de armazenamento obtido do método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) é um objeto de subarmazenamento.) Normalmente, os dados de rascunho e os instantâneos são armazenados em arquivos temporários, separados do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2dfec-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="2dfec-279">O efeito desses sinalizadores depende do número de leitores e/ou gravadores que acessam o armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="2dfec-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="2dfec-280">No caso de "gravador único", um objeto de armazenamento de modo transacionado é aberto para acesso de gravação e não pode haver nenhum outro acesso ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="2dfec-281">Ou seja, o arquivo é aberto com **STGM \_ transacionado**, acesso de **STGM \_ Write** ou **STGM \_ ReadWrite** e compartilhamento de **STGM \_ compartilhamento \_ exclusivo**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="2dfec-282">Nesse caso, as alterações no objeto de armazenamento são gravadas na área de rascunho.</span><span class="sxs-lookup"><span data-stu-id="2dfec-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="2dfec-283">Quando essas alterações são confirmadas, elas são copiadas para o armazenamento original.</span><span class="sxs-lookup"><span data-stu-id="2dfec-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="2dfec-284">Portanto, se nenhuma alteração for realmente feita no objeto de armazenamento, não haverá transferência de dados desnecessária.</span><span class="sxs-lookup"><span data-stu-id="2dfec-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="2dfec-285">No caso de "vários autores", um objeto de armazenamento transacionado é aberto para acesso de gravação, mas é compartilhado no asway como para permitir outros gravadores.</span><span class="sxs-lookup"><span data-stu-id="2dfec-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="2dfec-286">Ou seja, o objeto de armazenamento é aberto **com \_ STGM transacionado**, acesso de **STGM \_ Write** ou **STGM \_ ReadWrite** e compartilhamento de **\_ \_ \_ leitura de negação de compartilhamento de STGM**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="2dfec-287">Se o compartilhamento **de \_ STGM \_ compartilhamento \_** não for especificado, o caso será "vários gravadores, vários leitores".</span><span class="sxs-lookup"><span data-stu-id="2dfec-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="2dfec-288">Nesses casos, um instantâneo dos dados originais será feito durante a operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="2dfec-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="2dfec-289">Portanto, mesmo que nenhuma alteração seja feita no armazenamento e/ou não seja realmente aberta por outro gravador simultaneamente, a transferência de dados ainda é necessária durante a abertura.</span><span class="sxs-lookup"><span data-stu-id="2dfec-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="2dfec-290">Como resultado, o melhor desempenho em tempo de execução pode ser obtido abrindo o objeto de armazenamento nos modos **STGM \_ compartilhamento \_ Deny \_ Write** ou **STGM \_ share \_ exclusivo** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="2dfec-291">Para obter mais informações sobre como as alterações são confirmadas quando há vários gravadores, consulte [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="2dfec-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="2dfec-292">No caso de "gravador único, vários leitores", um objeto de armazenamento transacionado é aberto para acesso de gravação, mas é compartilhado com leitores.</span><span class="sxs-lookup"><span data-stu-id="2dfec-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="2dfec-293">Ou seja, o objeto de armazenamento é aberto pelo gravador com **STGM \_ transacionado**, acesso de **STGM \_ ReadWrite** ou **STGM \_ Write** e compartilhamento **de \_ \_ \_ gravação de negação de compartilhamento de STGM**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="2dfec-294">O armazenamento é aberto por leitores com **STGM \_ transacionado**, acesso de **STGM \_ Read** e compartilhamento de **STGM \_ share \_ Deny \_ None**.</span><span class="sxs-lookup"><span data-stu-id="2dfec-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="2dfec-295">Nesse caso, o gravador usa a área de rascunho para armazenar alterações não confirmadas.</span><span class="sxs-lookup"><span data-stu-id="2dfec-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="2dfec-296">Como nos casos acima, o leitor incorre em uma penalidade de desempenho em tempo de aberto enquanto uma cópia de instantâneo dos dados é criada.</span><span class="sxs-lookup"><span data-stu-id="2dfec-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="2dfec-297">Normalmente, a área de rascunho é um arquivo temporário, separado dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="2dfec-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="2dfec-298">Quando as alterações são confirmadas no arquivo original, os dados devem ser transferidos do arquivo temporário.</span><span class="sxs-lookup"><span data-stu-id="2dfec-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="2dfec-299">Para evitar essa transferência de dados, o sinalizador **\_ noscratch STGM** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="2dfec-300">Quando esse sinalizador é especificado, partes do arquivo de objeto de armazenamento são usadas para a área de rascunho, em vez de um arquivo temporário separado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="2dfec-301">Como resultado, as alterações de confirmação podem ser executadas rapidamente, pois pouca transferência de dados é necessária.</span><span class="sxs-lookup"><span data-stu-id="2dfec-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="2dfec-302">A desvantagem é que o arquivo de armazenamento pode se tornar maior do que seria, pois ele deve ser aumentado para ser grande o suficiente para os dados originais e para a área de rascunho.</span><span class="sxs-lookup"><span data-stu-id="2dfec-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="2dfec-303">Para consolidar os dados e remover essa área desnecessária, reabra o armazenamento raiz no modo transacionado, mas sem definir o sinalizador **\_ noscratch STGM** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="2dfec-304">Em seguida, chame [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) com o sinalizador de **\_ consolidação de STGC** definido.</span><span class="sxs-lookup"><span data-stu-id="2dfec-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="2dfec-305">A área de instantâneo, como a área de rascunho, também é, normalmente, um arquivo temporário, e isso também pode ser afetado com um sinalizador STGM.</span><span class="sxs-lookup"><span data-stu-id="2dfec-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="2dfec-306">Ao especificar o **sinalizador \_ nosnapshot STGM** , um arquivo de instantâneo temporário separado não é criado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="2dfec-307">Em vez disso, os dados originais nunca são modificados, mesmo se houver um ou mais gravadores por objeto.</span><span class="sxs-lookup"><span data-stu-id="2dfec-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="2dfec-308">Quando as alterações são confirmadas, elas são adicionadas ao arquivo, mas os dados originais permanecem intactos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="2dfec-309">Esse modo aumenta a eficiência, pois reduz o tempo de execução eliminando a necessidade de criar um instantâneo durante a operação de abertura.</span><span class="sxs-lookup"><span data-stu-id="2dfec-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="2dfec-310">No entanto, o uso desse modo pode resultar em um arquivo de armazenamento muito grande porque os dados no arquivo nunca podem ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="2dfec-311">Esse não é um limite para o tamanho dos arquivos abertos no modo nosnapshot.</span><span class="sxs-lookup"><span data-stu-id="2dfec-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="2dfec-312">Gravador único direto, modo de Multiple-Reader</span><span class="sxs-lookup"><span data-stu-id="2dfec-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="2dfec-313">Conforme descrito, é possível ter um único gravador e vários leitores de um objeto de armazenamento, se esse objeto for aberto no modo transacionado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="2dfec-314">Também é possível atingir o único gravador, caso de multileitura no modo direto, especificando o sinalizador **\_ \_ SWMR direto STGM** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="2dfec-315">No **modo \_ \_ SWMR direto do STGM** , é possível que um chamador Abra um objeto para acesso de leitura/gravação, enquanto outros chamadores simultaneamente têm o arquivo aberto para acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2dfec-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="2dfec-316">Não é válido usar esse sinalizador em combinação com o sinalizador **\_ transacionado STGM** .</span><span class="sxs-lookup"><span data-stu-id="2dfec-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="2dfec-317">Nesse modo, o gravador abre o objeto com os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="2dfec-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="2dfec-318">**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**</span><span class="sxs-lookup"><span data-stu-id="2dfec-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="2dfec-319">e cada um dos leitores abre o objeto com estes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="2dfec-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="2dfec-320">**STGM \_ \_SWMR direto** \| **STGM \_ ler** \| **STGM \_ compartilhamento \_ negar \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="2dfec-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="2dfec-321">Nesse modo, para modificar o objeto de armazenamento, o gravador deve obter acesso exclusivo ao objeto.</span><span class="sxs-lookup"><span data-stu-id="2dfec-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="2dfec-322">Isso é possível quando todos os leitores o fecharam.</span><span class="sxs-lookup"><span data-stu-id="2dfec-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="2dfec-323">O gravador usa a interface [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) para obter esse acesso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="2dfec-324">Modo simples</span><span class="sxs-lookup"><span data-stu-id="2dfec-324">Simple Mode</span></span>

<span data-ttu-id="2dfec-325">O modo simples (**STGM \_ simples**) é útil para aplicativos que executam operações de salvamento completas.</span><span class="sxs-lookup"><span data-stu-id="2dfec-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="2dfec-326">Ele é eficiente, mas tem as seguintes restrições:</span><span class="sxs-lookup"><span data-stu-id="2dfec-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="2dfec-327">Não existe suporte para subarmazenamentos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="2dfec-328">O objeto de armazenamento e os objetos de fluxo obtidos dele não podem ser empacotados.</span><span class="sxs-lookup"><span data-stu-id="2dfec-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="2dfec-329">Cada fluxo tem um tamanho mínimo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-329">Each stream has a minimum size.</span></span> <span data-ttu-id="2dfec-330">Se menos do que os bytes mínimos forem gravados em um fluxo quando o fluxo for liberado, o fluxo será estendido para o tamanho mínimo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="2dfec-331">Por exemplo, o tamanho mínimo para uma implementação de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) específica é de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="2dfec-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="2dfec-332">Um fluxo é criado e 1 KB é gravado nele.</span><span class="sxs-lookup"><span data-stu-id="2dfec-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="2dfec-333">Na versão final desse **IStream**, o tamanho do fluxo será estendido automaticamente para 4 KB.</span><span class="sxs-lookup"><span data-stu-id="2dfec-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="2dfec-334">Subsequentemente, abrir o fluxo e chamar o método [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) mostrará um tamanho de 4 KB.</span><span class="sxs-lookup"><span data-stu-id="2dfec-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="2dfec-335">Nem todos os métodos de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) terão suporte da implementação.</span><span class="sxs-lookup"><span data-stu-id="2dfec-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="2dfec-336">Para obter mais informações, consulte [implementação de arquivo composto por IStorage](istorage-compound-file-implementation.md)e [implementação de arquivo composto por IStream](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="2dfec-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="2dfec-337">O [marshaling](/windows/desktop/Midl/marshaling-ole-data-types) é o processo de empacotamento, desempacotamento e envio de parâmetros de método de interface entre limites de thread ou processo dentro de uma RPC (chamada de procedimento remoto).</span><span class="sxs-lookup"><span data-stu-id="2dfec-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="2dfec-338">Para obter mais informações, consulte [detalhes de marshaling](../com/marshaling-details.md) e [marshaling de interface](../com/interface-marshaling.md).</span><span class="sxs-lookup"><span data-stu-id="2dfec-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="2dfec-339">Quando um objeto de armazenamento é obtido por uma operação de criação no modo simples:</span><span class="sxs-lookup"><span data-stu-id="2dfec-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="2dfec-340">Elementos de fluxo podem ser criados, mas não abertos.</span><span class="sxs-lookup"><span data-stu-id="2dfec-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="2dfec-341">Quando um elemento de fluxo é criado chamando [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), não é possível criar outro fluxo até que esse objeto de fluxo seja liberado.</span><span class="sxs-lookup"><span data-stu-id="2dfec-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="2dfec-342">Depois que todos os fluxos forem gravados, chame [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) para liberar as alterações.</span><span class="sxs-lookup"><span data-stu-id="2dfec-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="2dfec-343">Quando um objeto de armazenamento é obtido por uma operação Open no modo simples:</span><span class="sxs-lookup"><span data-stu-id="2dfec-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="2dfec-344">É possível abrir apenas um elemento de fluxo por vez.</span><span class="sxs-lookup"><span data-stu-id="2dfec-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="2dfec-345">Não é possível alterar o tamanho de um fluxo chamando o método [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) ou buscando ou escrevendo além do final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="2dfec-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="2dfec-346">No entanto, como todos os fluxos têm um tamanho mínimo, é possível usar o fluxo até esse tamanho, mesmo que menos dados tenham sido gravados originalmente nele.</span><span class="sxs-lookup"><span data-stu-id="2dfec-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="2dfec-347">Para determinar o tamanho de um fluxo, use o método [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .</span><span class="sxs-lookup"><span data-stu-id="2dfec-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="2dfec-348">Lembre-se de que, se um elemento de armazenamento for modificado por um objeto de armazenamento que não está no modo simples, não será possível, novamente, abrir esse elemento de armazenamento no modo simples.</span><span class="sxs-lookup"><span data-stu-id="2dfec-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dfec-349">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dfec-349">Requirements</span></span>



| <span data-ttu-id="2dfec-350">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dfec-350">Requirement</span></span> | <span data-ttu-id="2dfec-351">Valor</span><span class="sxs-lookup"><span data-stu-id="2dfec-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfec-352">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dfec-352">Minimum supported client</span></span><br/> | <span data-ttu-id="2dfec-353">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2dfec-354">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dfec-354">Minimum supported server</span></span><br/> | <span data-ttu-id="2dfec-355">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2dfec-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2dfec-356">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2dfec-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dfec-357"><dt>ObjBase. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dfec-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dfec-358">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dfec-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dfec-359">**ISequentialStream:: ler**</span><span class="sxs-lookup"><span data-stu-id="2dfec-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="2dfec-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="2dfec-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="2dfec-361">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="2dfec-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="2dfec-362">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="2dfec-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="2dfec-363">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="2dfec-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="2dfec-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="2dfec-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="2dfec-365">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="2dfec-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="2dfec-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="2dfec-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

