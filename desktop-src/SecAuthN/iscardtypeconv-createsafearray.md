---
description: Cria um SAFEARRAY de automação de caracteres não assinados (bytes).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Método ISCardTypeConv:: createsafearray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089844"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="6b46d-103">Método ISCardTypeConv:: createsafearray</span><span class="sxs-lookup"><span data-stu-id="6b46d-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="6b46d-104">\[O método **createsafearray** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6b46d-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b46d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6b46d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b46d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6b46d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6b46d-107">O método **createsafearray** cria um SafeArray de automação de caracteres não assinados (bytes).</span><span class="sxs-lookup"><span data-stu-id="6b46d-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b46d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b46d-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="6b46d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b46d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b46d-110">*nAllocSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b46d-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b46d-111">Tamanho em bytes da memória a ser alocada para a matriz.</span><span class="sxs-lookup"><span data-stu-id="6b46d-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="6b46d-112">*ppArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b46d-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b46d-113">Ponteiro para o objeto SAFEARRAY a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="6b46d-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b46d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b46d-114">Return value</span></span>

<span data-ttu-id="6b46d-115">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="6b46d-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="6b46d-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6b46d-116">Return code</span></span>                                                                                   | <span data-ttu-id="6b46d-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b46d-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b46d-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6b46d-119">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b46d-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6b46d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6b46d-121">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="6b46d-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="6b46d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b46d-123">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="6b46d-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="6b46d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b46d-124">Remarks</span></span>

<span data-ttu-id="6b46d-125">Para criar uma matriz de bytes C/C++ típica, chame [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="6b46d-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="6b46d-126">Para criar um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)), chame [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6b46d-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b46d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b46d-127">Requirements</span></span>



| <span data-ttu-id="6b46d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b46d-128">Requirement</span></span> | <span data-ttu-id="6b46d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6b46d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b46d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b46d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6b46d-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b46d-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6b46d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b46d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6b46d-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b46d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b46d-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6b46d-134">End of client support</span></span><br/>    | <span data-ttu-id="6b46d-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b46d-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6b46d-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6b46d-136">End of server support</span></span><br/>    | <span data-ttu-id="6b46d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b46d-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6b46d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b46d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b46d-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b46d-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b46d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b46d-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b46d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6b46d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b46d-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b46d-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6b46d-144">IID</span><span class="sxs-lookup"><span data-stu-id="6b46d-144">IID</span></span><br/>                      | <span data-ttu-id="6b46d-145">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6b46d-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6b46d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b46d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b46d-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="6b46d-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="6b46d-148">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="6b46d-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="6b46d-149">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="6b46d-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="6b46d-150">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="6b46d-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
