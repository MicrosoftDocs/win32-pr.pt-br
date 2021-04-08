---
description: Converte uma matriz de bytes definida como um SAFEARRAY em um buffer universal de bytes (objeto IStream).
ms.assetid: faa07bb5-cfdb-4181-b86a-f82a9c6b251a
title: 'Método ISCardTypeConv:: ConvertSafeArrayToByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertSafeArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa6503f474d96e3c25da3f2780ac43976b6507a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920856"
---
# <a name="iscardtypeconvconvertsafearraytobytebuffer-method"></a><span data-ttu-id="b6959-103">Método ISCardTypeConv:: ConvertSafeArrayToByteBuffer</span><span class="sxs-lookup"><span data-stu-id="b6959-103">ISCardTypeConv::ConvertSafeArrayToByteBuffer method</span></span>

<span data-ttu-id="b6959-104">\[O método **ConvertSafeArrayToByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6959-104">\[The **ConvertSafeArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6959-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b6959-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6959-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b6959-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b6959-107">O método **ConvertSafeArrayToByteBuffer** converte uma matriz de bytes definida como um SafeArray em um buffer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="b6959-107">The **ConvertSafeArrayToByteBuffer** method converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="b6959-108">O buffer de bytes criado é um fluxo mapeado em um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="b6959-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="b6959-109">Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b6959-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="b6959-110">Um recurso exclusivo sobre essa implementação de matriz é que quando você chama o método **IStream:: Release** , a memória subjacente será liberada para você.</span><span class="sxs-lookup"><span data-stu-id="b6959-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6959-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6959-111">Syntax</span></span>


```C++
HRESULT ConvertSafeArrayToByteBuffer(
  [in]  LPSAFEARRAY  pbyArray,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="b6959-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6959-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6959-113">*pbyArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6959-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6959-114">Ponteiro para o SAFEARRAY a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="b6959-114">Pointer to the SAFEARRAY to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="b6959-115">*ppbyBuff* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6959-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6959-116">Ponteiro para o objeto **IStream** a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="b6959-116">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6959-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6959-117">Return value</span></span>

<span data-ttu-id="b6959-118">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="b6959-118">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b6959-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6959-119">Return code</span></span>                                                                                   | <span data-ttu-id="b6959-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6959-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6959-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6959-122">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b6959-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b6959-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b6959-124">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="b6959-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="b6959-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b6959-126">Um parâmetro de tipo de ponteiro estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="b6959-126">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b6959-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6959-128">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="b6959-128">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b6959-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6959-129">Remarks</span></span>

<span data-ttu-id="b6959-130">A memória alocada é móvel.</span><span class="sxs-lookup"><span data-stu-id="b6959-130">Memory allocated is moveable.</span></span> <span data-ttu-id="b6959-131">Use o método **IStream:: Release** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="b6959-131">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6959-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6959-132">Requirements</span></span>



| <span data-ttu-id="b6959-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6959-133">Requirement</span></span> | <span data-ttu-id="b6959-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b6959-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6959-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6959-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b6959-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6959-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b6959-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6959-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b6959-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6959-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b6959-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b6959-139">End of client support</span></span><br/>    | <span data-ttu-id="b6959-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6959-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b6959-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b6959-141">End of server support</span></span><br/>    | <span data-ttu-id="b6959-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6959-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b6959-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6959-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6959-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6959-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6959-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6959-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6959-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b6959-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6959-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6959-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6959-149">IID</span><span class="sxs-lookup"><span data-stu-id="b6959-149">IID</span></span><br/>                      | <span data-ttu-id="b6959-150">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b6959-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b6959-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6959-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6959-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="b6959-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="b6959-153">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b6959-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
