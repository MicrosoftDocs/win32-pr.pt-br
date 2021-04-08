---
description: A interface IByteBuffer é fornecida para ler, gravar e gerenciar objetos Stream. Esse objeto essencialmente é um wrapper para o objeto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interface IByteBuffer (Scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922523"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="72c6f-104">Interface IByteBuffer</span><span class="sxs-lookup"><span data-stu-id="72c6f-104">IByteBuffer interface</span></span>

<span data-ttu-id="72c6f-105">\[A interface **IByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="72c6f-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72c6f-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="72c6f-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="72c6f-107">A interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="72c6f-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="72c6f-108">A interface **IByteBuffer** é fornecida para ler, gravar e gerenciar objetos Stream.</span><span class="sxs-lookup"><span data-stu-id="72c6f-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="72c6f-109">Esse objeto essencialmente é um wrapper para o objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="72c6f-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="72c6f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="72c6f-110">Members</span></span>

<span data-ttu-id="72c6f-111">A interface **IByteBuffer** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="72c6f-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="72c6f-112">**IByteBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="72c6f-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="72c6f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c6f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72c6f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="72c6f-114">Methods</span></span>

<span data-ttu-id="72c6f-115">A interface **IByteBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="72c6f-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="72c6f-116">Método</span><span class="sxs-lookup"><span data-stu-id="72c6f-116">Method</span></span>                                           | <span data-ttu-id="72c6f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="72c6f-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72c6f-118">**8i**</span><span class="sxs-lookup"><span data-stu-id="72c6f-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="72c6f-119">Clona um objeto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="72c6f-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="72c6f-120">**Compromisso**</span><span class="sxs-lookup"><span data-stu-id="72c6f-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="72c6f-121">Confirma uma [*transação*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="72c6f-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="72c6f-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="72c6f-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="72c6f-123">Copia bytes para outro objeto.</span><span class="sxs-lookup"><span data-stu-id="72c6f-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="72c6f-124">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="72c6f-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="72c6f-125">Inicializa o objeto **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="72c6f-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="72c6f-126">**LockRegion**</span><span class="sxs-lookup"><span data-stu-id="72c6f-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="72c6f-127">Restringe o acesso a um intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="72c6f-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="72c6f-128">**Ler**</span><span class="sxs-lookup"><span data-stu-id="72c6f-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="72c6f-129">Lê bytes na memória.</span><span class="sxs-lookup"><span data-stu-id="72c6f-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="72c6f-130">**Voltar**</span><span class="sxs-lookup"><span data-stu-id="72c6f-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="72c6f-131">Descarta as alterações desde a última chamada de [**confirmação**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="72c6f-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="72c6f-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="72c6f-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="72c6f-133">Altera o ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="72c6f-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="72c6f-134">**Size**</span><span class="sxs-lookup"><span data-stu-id="72c6f-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="72c6f-135">Altera o tamanho do objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="72c6f-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="72c6f-136">**Stat**</span><span class="sxs-lookup"><span data-stu-id="72c6f-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="72c6f-137">Recupera informações estatísticas sobre um fluxo.</span><span class="sxs-lookup"><span data-stu-id="72c6f-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="72c6f-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="72c6f-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="72c6f-139">Remove a restrição de acesso definida anteriormente por [**LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="72c6f-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="72c6f-140">**Gravar**</span><span class="sxs-lookup"><span data-stu-id="72c6f-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="72c6f-141">Grava bytes no fluxo.</span><span class="sxs-lookup"><span data-stu-id="72c6f-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="72c6f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c6f-142">Requirements</span></span>



| <span data-ttu-id="72c6f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c6f-143">Requirement</span></span> | <span data-ttu-id="72c6f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="72c6f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72c6f-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72c6f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="72c6f-146">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72c6f-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72c6f-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72c6f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="72c6f-148">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72c6f-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72c6f-149">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="72c6f-149">End of client support</span></span><br/>    | <span data-ttu-id="72c6f-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72c6f-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="72c6f-151">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="72c6f-151">End of server support</span></span><br/>    | <span data-ttu-id="72c6f-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72c6f-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="72c6f-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72c6f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c6f-154"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c6f-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="72c6f-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="72c6f-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="72c6f-156"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="72c6f-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="72c6f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="72c6f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72c6f-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72c6f-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="72c6f-159">IID</span><span class="sxs-lookup"><span data-stu-id="72c6f-159">IID</span></span><br/>                      | <span data-ttu-id="72c6f-160">IID \_ IByteBuffer é definido como E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="72c6f-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

