---
description: Cria um buffer universal de bytes mapeados em um objeto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: 'Método ISCardTypeConv:: CreateByteBuffer (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011083"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a><span data-ttu-id="b1539-103">Método ISCardTypeConv:: CreateByteBuffer</span><span class="sxs-lookup"><span data-stu-id="b1539-103">ISCardTypeConv::CreateByteBuffer method</span></span>

<span data-ttu-id="b1539-104">\[O método **CreateByteBuffer** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b1539-104">\[The **CreateByteBuffer** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1539-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b1539-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b1539-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b1539-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b1539-107">O método **CreateByteBuffer** cria um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="b1539-107">The **CreateByteBuffer** method creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span>

<span data-ttu-id="b1539-108">O buffer de bytes criado é um fluxo mapeado em um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="b1539-108">The byte buffer created is a stream mapped over a memory block.</span></span> <span data-ttu-id="b1539-109">Para acessar ou gerenciar o buffer, use os métodos fornecidos pela interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="b1539-109">To access or manage the buffer, use the methods provided by the **IStream** interface.</span></span> <span data-ttu-id="b1539-110">Um recurso exclusivo sobre essa implementação de matriz é que quando você chama o método **IStream:: Release** , a memória subjacente será liberada para você.</span><span class="sxs-lookup"><span data-stu-id="b1539-110">A unique feature about this array implementation is that when you call the **IStream::Release** method, the underlying memory will be released for you.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1539-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1539-111">Syntax</span></span>


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a><span data-ttu-id="b1539-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1539-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1539-113">*dwAllocSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1539-113">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1539-114">Tamanho em bytes da memória a ser alocada para a matriz.</span><span class="sxs-lookup"><span data-stu-id="b1539-114">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="b1539-115">*ppbyBuff* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1539-115">*ppbyBuff* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1539-116">Ponteiro para o objeto IStream a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="b1539-116">Pointer to the IStream object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1539-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1539-117">Return value</span></span>

<span data-ttu-id="b1539-118">Os possíveis valores de retorno são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="b1539-118">The possible return values are the following:</span></span>



| <span data-ttu-id="b1539-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1539-119">Return code</span></span>                                                                                   | <span data-ttu-id="b1539-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1539-120">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1539-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b1539-122">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b1539-122">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b1539-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b1539-124">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="b1539-124">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="b1539-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b1539-126">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1539-126">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b1539-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1539-127">Remarks</span></span>

<span data-ttu-id="b1539-128">A memória alocada é móvel.</span><span class="sxs-lookup"><span data-stu-id="b1539-128">Memory allocated is movable.</span></span> <span data-ttu-id="b1539-129">Use o método **IStream:: Release** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="b1539-129">Use the **IStream::Release** method to free the memory.</span></span>

<span data-ttu-id="b1539-130">Para criar uma matriz de bytes C/C++ típica, chame [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="b1539-130">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="b1539-131">Para criar um SAFEARRAY de automação de caracteres não assinados (bytes), chame [**createsafearray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="b1539-131">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1539-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1539-132">Requirements</span></span>



| <span data-ttu-id="b1539-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1539-133">Requirement</span></span> | <span data-ttu-id="b1539-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b1539-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1539-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1539-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b1539-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1539-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b1539-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1539-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b1539-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1539-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1539-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b1539-139">End of client support</span></span><br/>    | <span data-ttu-id="b1539-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1539-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b1539-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b1539-141">End of server support</span></span><br/>    | <span data-ttu-id="b1539-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1539-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b1539-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1539-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1539-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1539-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b1539-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1539-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1539-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b1539-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1539-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1539-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1539-149">IID</span><span class="sxs-lookup"><span data-stu-id="b1539-149">IID</span></span><br/>                      | <span data-ttu-id="b1539-150">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b1539-150">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b1539-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1539-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1539-152">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="b1539-152">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="b1539-153">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b1539-153">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="b1539-154">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="b1539-154">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="b1539-155">**Createsafearray**</span><span class="sxs-lookup"><span data-stu-id="b1539-155">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
