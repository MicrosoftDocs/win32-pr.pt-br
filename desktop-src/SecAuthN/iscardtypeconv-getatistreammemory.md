---
description: Adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface COM de IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'Método ISCardTypeConv:: GetAtIStreamMemory (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646783"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a><span data-ttu-id="d79e0-103">Método ISCardTypeConv:: GetAtIStreamMemory</span><span class="sxs-lookup"><span data-stu-id="d79e0-103">ISCardTypeConv::GetAtIStreamMemory method</span></span>

<span data-ttu-id="d79e0-104">\[O método **GetAtIStreamMemory** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d79e0-104">\[The **GetAtIStreamMemory** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d79e0-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d79e0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d79e0-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d79e0-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d79e0-107">O método **GetAtIStreamMemory** adquire um ponteiro de byte para o bloco de memória HGLOBAL que é gerenciado pela interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="d79e0-107">The **GetAtIStreamMemory** method acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span>

<span data-ttu-id="d79e0-108">Essa é uma maneira de obter a memória sob o **IStream** sem ter que obter o valor de sizeof para o bloco de memória em bytes e ler os bytes em uma matriz de bytes temporária usando a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="d79e0-108">This is a way to get at the memory under the **IStream** without having to get the sizeof value for the memory block in bytes and read the bytes into a temporary byte array using the **IStream** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d79e0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d79e0-109">Syntax</span></span>


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a><span data-ttu-id="d79e0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d79e0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d79e0-111">*pStrm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d79e0-111">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d79e0-112">Um ponteiro para a interface com **IStream** que gerencia o bloco de memória HGLOBAL.</span><span class="sxs-lookup"><span data-stu-id="d79e0-112">A pointer to the **IStream** COM interface that manages the HGLOBAL memory block.</span></span>

</dd> <dt>

<span data-ttu-id="d79e0-113">*ppMem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d79e0-113">*ppMem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d79e0-114">Um ponteiro para o primeiro byte do bloco de memória HGLOBAL se for bem-sucedido; caso contrário, **NULL** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="d79e0-114">A pointer to the first byte of the HGLOBAL memory block if successful; else, **NULL** if operation fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d79e0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d79e0-115">Return value</span></span>

<span data-ttu-id="d79e0-116">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d79e0-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d79e0-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d79e0-117">Return code</span></span>                                                                                   | <span data-ttu-id="d79e0-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d79e0-118">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d79e0-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d79e0-120">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d79e0-120">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d79e0-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d79e0-122">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="d79e0-122">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="d79e0-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d79e0-124">Um parâmetro de tipo de ponteiro estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="d79e0-124">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d79e0-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d79e0-126">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="d79e0-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d79e0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d79e0-127">Remarks</span></span>

<span data-ttu-id="d79e0-128">A contagem de referência de **IStream** será incrementada para cada ponteiro *ppMem* adquirido.</span><span class="sxs-lookup"><span data-stu-id="d79e0-128">The **IStream** reference count will be incremented for each *ppMem* pointer acquired.</span></span>

## <a name="requirements"></a><span data-ttu-id="d79e0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d79e0-129">Requirements</span></span>



| <span data-ttu-id="d79e0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d79e0-130">Requirement</span></span> | <span data-ttu-id="d79e0-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d79e0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d79e0-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d79e0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d79e0-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d79e0-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d79e0-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d79e0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d79e0-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d79e0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d79e0-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d79e0-136">End of client support</span></span><br/>    | <span data-ttu-id="d79e0-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d79e0-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d79e0-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d79e0-138">End of server support</span></span><br/>    | <span data-ttu-id="d79e0-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d79e0-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d79e0-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d79e0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d79e0-141"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-141"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="d79e0-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d79e0-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="d79e0-143"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-143"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d79e0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d79e0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d79e0-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d79e0-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d79e0-146">IID</span><span class="sxs-lookup"><span data-stu-id="d79e0-146">IID</span></span><br/>                      | <span data-ttu-id="d79e0-147">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d79e0-147">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d79e0-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="d79e0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79e0-149">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="d79e0-149">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="d79e0-150">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="d79e0-150">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
