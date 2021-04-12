---
description: Converte um buffer universal de bytes (objeto IStream) em uma matriz de bytes C/C++ típica.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'Método ISCardTypeConv:: ConvertByteBufferToByteArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170948"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="6ec4a-103">Método ISCardTypeConv:: ConvertByteBufferToByteArray</span><span class="sxs-lookup"><span data-stu-id="6ec4a-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="6ec4a-104">\[O método **ConvertByteBufferToByteArray** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6ec4a-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6ec4a-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6ec4a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6ec4a-107">O método **ConvertByteBufferToByteArray** converte um buffer universal de bytes (objeto **IStream** ) em uma matriz de bytes C/C++ típica.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec4a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ec4a-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="6ec4a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ec4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec4a-110">*pbyBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ec4a-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec4a-111">Ponteiro para o objeto **IStream** a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="6ec4a-112">*ppArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ec4a-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ec4a-113">Ponteiro para a matriz de bytes a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec4a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ec4a-114">Return value</span></span>

<span data-ttu-id="6ec4a-115">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="6ec4a-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="6ec4a-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ec4a-116">Return code</span></span>                                                                                   | <span data-ttu-id="6ec4a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ec4a-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ec4a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6ec4a-119">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6ec4a-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6ec4a-121">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="6ec4a-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6ec4a-123">Um parâmetro de tipo de ponteiro estava incorreto.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6ec4a-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6ec4a-125">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="6ec4a-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="6ec4a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec4a-126">Requirements</span></span>



| <span data-ttu-id="6ec4a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec4a-127">Requirement</span></span> | <span data-ttu-id="6ec4a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6ec4a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec4a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec4a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec4a-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ec4a-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ec4a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ec4a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec4a-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ec4a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ec4a-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6ec4a-133">End of client support</span></span><br/>    | <span data-ttu-id="6ec4a-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ec4a-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6ec4a-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6ec4a-135">End of server support</span></span><br/>    | <span data-ttu-id="6ec4a-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ec4a-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6ec4a-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ec4a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ec4a-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ec4a-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ec4a-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ec4a-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ec4a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec4a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec4a-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec4a-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ec4a-143">IID</span><span class="sxs-lookup"><span data-stu-id="6ec4a-143">IID</span></span><br/>                      | <span data-ttu-id="6ec4a-144">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6ec4a-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6ec4a-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ec4a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec4a-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="6ec4a-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="6ec4a-147">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="6ec4a-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
