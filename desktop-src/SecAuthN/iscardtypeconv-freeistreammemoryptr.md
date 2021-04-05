---
description: Libera o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado por uma interface COM de IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: 'Método ISCardTypeConv:: FreeIStreamMemoryPtr (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662280"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a><span data-ttu-id="af68a-103">Método ISCardTypeConv:: FreeIStreamMemoryPtr</span><span class="sxs-lookup"><span data-stu-id="af68a-103">ISCardTypeConv::FreeIStreamMemoryPtr method</span></span>

<span data-ttu-id="af68a-104">\[O método **FreeIStreamMemoryPtr** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="af68a-104">\[The **FreeIStreamMemoryPtr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af68a-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="af68a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af68a-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="af68a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af68a-107">O método **FreeIStreamMemoryPtr** libera o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado por uma interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="af68a-107">The **FreeIStreamMemoryPtr** method frees the byte pointer pointing to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="af68a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af68a-108">Syntax</span></span>


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a><span data-ttu-id="af68a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af68a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af68a-110">*pStrm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af68a-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af68a-111">Ponteiro para a interface **IStream** que gerencia o bloco de memória apontado pelo *pMem*.</span><span class="sxs-lookup"><span data-stu-id="af68a-111">Pointer to the **IStream** interface that manages the memory block pointed to by *pMem*.</span></span>

</dd> <dt>

<span data-ttu-id="af68a-112">*pMem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af68a-112">*pMem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af68a-113">Ponteiro para o bloco de memória gerenciado pela interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="af68a-113">Pointer to the memory block managed by the **IStream** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af68a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af68a-114">Return value</span></span>

<span data-ttu-id="af68a-115">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="af68a-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="af68a-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="af68a-116">Return code</span></span>                                                                                   | <span data-ttu-id="af68a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="af68a-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="af68a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af68a-119">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="af68a-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="af68a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af68a-121">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="af68a-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="af68a-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="af68a-123">Um parâmetro de tipo de ponteiro estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="af68a-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="af68a-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af68a-125">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="af68a-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="af68a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="af68a-126">Remarks</span></span>

<span data-ttu-id="af68a-127">Essa função libera completamente e limpa o ponteiro de byte apontando para o bloco de memória HGLOBAL gerenciado pela interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="af68a-127">This function completely and cleanly releases the byte pointer pointing to the HGLOBAL memory block managed by the **IStream** interface.</span></span> <span data-ttu-id="af68a-128">O ponteiro de byte é adquirido por uma chamada para [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span><span class="sxs-lookup"><span data-stu-id="af68a-128">The byte pointer is acquired by a call to [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af68a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af68a-129">Requirements</span></span>



| <span data-ttu-id="af68a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="af68a-130">Requirement</span></span> | <span data-ttu-id="af68a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="af68a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af68a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af68a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="af68a-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af68a-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af68a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af68a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="af68a-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af68a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af68a-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="af68a-136">End of client support</span></span><br/>    | <span data-ttu-id="af68a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af68a-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af68a-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="af68a-138">End of server support</span></span><br/>    | <span data-ttu-id="af68a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af68a-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af68a-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af68a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="af68a-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="af68a-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="af68a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="af68a-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af68a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af68a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af68a-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af68a-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af68a-146">IID</span><span class="sxs-lookup"><span data-stu-id="af68a-146">IID</span></span><br/>                      | <span data-ttu-id="af68a-147">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af68a-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="af68a-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="af68a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af68a-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="af68a-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="af68a-150">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="af68a-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="af68a-151">**GetAtIStreamMemory**</span><span class="sxs-lookup"><span data-stu-id="af68a-151">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
