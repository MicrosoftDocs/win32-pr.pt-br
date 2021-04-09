---
description: Cria uma matriz de bytes C/C++ típica.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'Método ISCardTypeConv:: CreateByteArray (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091660"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="1db5c-103">Método ISCardTypeConv:: CreateByteArray</span><span class="sxs-lookup"><span data-stu-id="1db5c-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="1db5c-104">\[O método **CreateByteArray** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1db5c-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1db5c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1db5c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1db5c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1db5c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1db5c-107">O método **CreateByteArray** cria uma matriz de bytes C/C++ típica.</span><span class="sxs-lookup"><span data-stu-id="1db5c-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db5c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1db5c-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="1db5c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1db5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1db5c-110">*dwAllocSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1db5c-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1db5c-111">Tamanho (em bytes) da memória a ser alocada para a matriz.</span><span class="sxs-lookup"><span data-stu-id="1db5c-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="1db5c-112">*ppbyArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1db5c-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1db5c-113">Ponteiro para a matriz de bytes a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="1db5c-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1db5c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1db5c-114">Return value</span></span>

<span data-ttu-id="1db5c-115">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="1db5c-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="1db5c-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1db5c-116">Return code</span></span>                                                                                   | <span data-ttu-id="1db5c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1db5c-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1db5c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1db5c-119">Memória alocada com êxito.</span><span class="sxs-lookup"><span data-stu-id="1db5c-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1db5c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1db5c-121">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="1db5c-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="1db5c-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1db5c-123">Não há memória livre suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="1db5c-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="1db5c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1db5c-124">Remarks</span></span>

<span data-ttu-id="1db5c-125">Para criar um buffer universal de bytes mapeados em um objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)), chame [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="1db5c-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="1db5c-126">Para criar um SAFEARRAY de automação de caracteres não assinados (bytes), chame [**createsafearray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="1db5c-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1db5c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1db5c-127">Requirements</span></span>



| <span data-ttu-id="1db5c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db5c-128">Requirement</span></span> | <span data-ttu-id="1db5c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1db5c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1db5c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1db5c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1db5c-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1db5c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1db5c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1db5c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1db5c-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1db5c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1db5c-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1db5c-134">End of client support</span></span><br/>    | <span data-ttu-id="1db5c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1db5c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1db5c-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1db5c-136">End of server support</span></span><br/>    | <span data-ttu-id="1db5c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1db5c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1db5c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1db5c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1db5c-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="1db5c-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1db5c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="1db5c-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1db5c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1db5c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1db5c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1db5c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1db5c-144">IID</span><span class="sxs-lookup"><span data-stu-id="1db5c-144">IID</span></span><br/>                      | <span data-ttu-id="1db5c-145">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1db5c-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1db5c-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1db5c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db5c-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="1db5c-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="1db5c-148">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="1db5c-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="1db5c-149">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="1db5c-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="1db5c-150">**Createsafearray**</span><span class="sxs-lookup"><span data-stu-id="1db5c-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
