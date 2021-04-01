---
description: Converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (objeto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'Método ISCardTypeConv:: ConvertByteArrayToByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829749"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a><span data-ttu-id="176b8-103">Método ISCardTypeConv:: ConvertByteArrayToByteBuffer</span><span class="sxs-lookup"><span data-stu-id="176b8-103">ISCardTypeConv::ConvertByteArrayToByteBuffer method</span></span>

<span data-ttu-id="176b8-104">\[O método **ConvertByteArrayToByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="176b8-104">\[The **ConvertByteArrayToByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="176b8-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="176b8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="176b8-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="176b8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="176b8-107">O método **ConvertByteArrayToByteBuffer** converte uma matriz de bytes C/C++ típica em um buffer universal de bytes (objeto **IStream** ).</span><span class="sxs-lookup"><span data-stu-id="176b8-107">The **ConvertByteArrayToByteBuffer** method converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span>

<span data-ttu-id="176b8-108">O buffer de bytes criado é um fluxo mapeado em um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="176b8-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="176b8-109">Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="176b8-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="176b8-110">Um recurso exclusivo sobre essa implementação de matriz é que quando você chama o método **IStream:: Release** , a memória subjacente será liberada para você.</span><span class="sxs-lookup"><span data-stu-id="176b8-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="176b8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="176b8-111">Syntax</span></span>


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="176b8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="176b8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="176b8-113">*pbyArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="176b8-113">*pbyArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176b8-114">Ponteiro para a matriz de bytes a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="176b8-114">Pointer to the array of bytes to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="176b8-115">*dwArraySize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="176b8-115">*dwArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176b8-116">Tamanho da matriz de bytes a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="176b8-116">Size of the byte array to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="176b8-117">*ppbyBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="176b8-117">*ppbyBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="176b8-118">Ponteiro para o objeto **IStream** a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="176b8-118">Pointer to the **IStream** object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="176b8-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="176b8-119">Return value</span></span>

<span data-ttu-id="176b8-120">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="176b8-120">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="176b8-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="176b8-121">Return code</span></span>                                                                                   | <span data-ttu-id="176b8-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="176b8-122">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="176b8-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="176b8-124">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="176b8-124">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="176b8-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="176b8-126">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="176b8-126">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="176b8-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="176b8-128">Um parâmetro de tipo de ponteiro estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="176b8-128">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="176b8-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="176b8-130">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="176b8-130">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="176b8-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="176b8-131">Remarks</span></span>

<span data-ttu-id="176b8-132">A memória alocada é móvel.</span><span class="sxs-lookup"><span data-stu-id="176b8-132">Memory allocated is movable.</span></span> <span data-ttu-id="176b8-133">Use o método **IStream:: Release** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="176b8-133">Use the **IStream::Release** method to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="176b8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="176b8-134">Requirements</span></span>



| <span data-ttu-id="176b8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="176b8-135">Requirement</span></span> | <span data-ttu-id="176b8-136">Valor</span><span class="sxs-lookup"><span data-stu-id="176b8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="176b8-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="176b8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="176b8-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="176b8-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="176b8-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="176b8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="176b8-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="176b8-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="176b8-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="176b8-141">End of client support</span></span><br/>    | <span data-ttu-id="176b8-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="176b8-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="176b8-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="176b8-143">End of server support</span></span><br/>    | <span data-ttu-id="176b8-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="176b8-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="176b8-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="176b8-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="176b8-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="176b8-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="176b8-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="176b8-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="176b8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="176b8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="176b8-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="176b8-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="176b8-151">IID</span><span class="sxs-lookup"><span data-stu-id="176b8-151">IID</span></span><br/>                      | <span data-ttu-id="176b8-152">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="176b8-152">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="176b8-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="176b8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176b8-154">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="176b8-154">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="176b8-155">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="176b8-155">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
