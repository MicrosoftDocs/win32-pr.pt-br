---
description: Fornece os métodos necessários para dar suporte aos usuários das outras interfaces COM de cartão inteligente.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interface ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828349"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="a0b22-103">Interface ISCardTypeConv</span><span class="sxs-lookup"><span data-stu-id="a0b22-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="a0b22-104">\[A interface **ISCardTypeConv** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a0b22-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0b22-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a0b22-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0b22-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a0b22-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a0b22-107">A interface **ISCardTypeConv** fornece os métodos necessários para dar suporte aos usuários das outras interfaces com de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a0b22-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="a0b22-108">Essa interface é fornecida apenas para fins de compatibilidade com versões anteriores e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="a0b22-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="a0b22-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a0b22-109">Members</span></span>

<span data-ttu-id="a0b22-110">A interface **ISCardTypeConv** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a0b22-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a0b22-111">**ISCardTypeConv** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a0b22-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="a0b22-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0b22-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0b22-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0b22-113">Methods</span></span>

<span data-ttu-id="a0b22-114">A interface **ISCardTypeConv** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a0b22-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="a0b22-115">Método</span><span class="sxs-lookup"><span data-stu-id="a0b22-115">Method</span></span>                                                                              | <span data-ttu-id="a0b22-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0b22-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0b22-117">**ConvertByteArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0b22-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="a0b22-118">Converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="a0b22-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="a0b22-119">**ConvertByteBufferToByteArray**</span><span class="sxs-lookup"><span data-stu-id="a0b22-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="a0b22-120">Converte uma matriz de bytes mapeada em um buffer universal de bytes (objeto **IStream** ) em uma matriz de bytes C/C++ típica.</span><span class="sxs-lookup"><span data-stu-id="a0b22-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="a0b22-121">**ConvertByteBufferToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="a0b22-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="a0b22-122">Converte uma matriz de bytes mapeada em um buffer universal de bytes (objeto **IStream** ) em um SafeArray de Char (Byte) não assinado.</span><span class="sxs-lookup"><span data-stu-id="a0b22-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="a0b22-123">**ConvertSafeArrayToByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0b22-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="a0b22-124">Converte uma matriz de bytes definida como um SAFEARRAY em um buffer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="a0b22-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="a0b22-125">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="a0b22-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="a0b22-126">Cria uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="a0b22-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a0b22-127">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0b22-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="a0b22-128">Cria um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="a0b22-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="a0b22-129">**Createsafearray**</span><span class="sxs-lookup"><span data-stu-id="a0b22-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="a0b22-130">Cria um SAFEARRAY de automação de caracteres não assinados (bytes).</span><span class="sxs-lookup"><span data-stu-id="a0b22-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="a0b22-131">**FreeIStreamMemoryPtr**</span><span class="sxs-lookup"><span data-stu-id="a0b22-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="a0b22-132">Libera um ponteiro de memória para o bloco de memória HGLOBAL gerenciado por uma interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a0b22-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="a0b22-133">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="a0b22-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="a0b22-134">Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a0b22-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="a0b22-135">**SizeOfIStream**</span><span class="sxs-lookup"><span data-stu-id="a0b22-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="a0b22-136">Determina o tamanho (número de bytes) de uma interface com com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a0b22-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="a0b22-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0b22-137">Requirements</span></span>



| <span data-ttu-id="a0b22-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b22-138">Requirement</span></span> | <span data-ttu-id="a0b22-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a0b22-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b22-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0b22-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b22-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0b22-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0b22-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0b22-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b22-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0b22-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0b22-144">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a0b22-144">End of client support</span></span><br/>    | <span data-ttu-id="a0b22-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0b22-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a0b22-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a0b22-146">End of server support</span></span><br/>    | <span data-ttu-id="a0b22-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0b22-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a0b22-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0b22-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b22-149"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b22-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0b22-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a0b22-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0b22-151"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0b22-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0b22-152">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b22-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b22-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b22-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0b22-154">IID</span><span class="sxs-lookup"><span data-stu-id="a0b22-154">IID</span></span><br/>                      | <span data-ttu-id="a0b22-155">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a0b22-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
