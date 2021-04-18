---
description: Determina o tamanho, em bytes, da interface COM de IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'Método ISCardTypeConv:: SizeOfIStream (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751525"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="01990-103">Método ISCardTypeConv:: SizeOfIStream</span><span class="sxs-lookup"><span data-stu-id="01990-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="01990-104">\[O método **SizeOfIStream** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="01990-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="01990-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="01990-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="01990-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="01990-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="01990-107">O método **SizeOfIStream** determina o tamanho, em bytes, da interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="01990-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="01990-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01990-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="01990-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01990-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01990-110">*pStrm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01990-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01990-111">Um ponteiro para a interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="01990-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="01990-112">*puliSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01990-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01990-113">Um ponteiro para o inteiro grande não assinado que pode conter o valor de sizeof de 64 bits inteiro da interface com de **IStream** .</span><span class="sxs-lookup"><span data-stu-id="01990-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01990-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01990-114">Return value</span></span>

<span data-ttu-id="01990-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="01990-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="01990-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01990-116">Return code</span></span>                                                                                  | <span data-ttu-id="01990-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="01990-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01990-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01990-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="01990-119">A função teve êxito e *\* puliSize* é o tamanho, em bytes, da interface com de IStream.</span><span class="sxs-lookup"><span data-stu-id="01990-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="01990-120"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="01990-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="01990-121">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="01990-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="01990-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="01990-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="01990-123">O parâmetro *puliSize* está incorreto.</span><span class="sxs-lookup"><span data-stu-id="01990-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="01990-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="01990-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="01990-125">O parâmetro *pStrm* está incorreto.</span><span class="sxs-lookup"><span data-stu-id="01990-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="01990-126"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="01990-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="01990-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="01990-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="01990-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01990-128">Requirements</span></span>



| <span data-ttu-id="01990-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="01990-129">Requirement</span></span> | <span data-ttu-id="01990-130">Valor</span><span class="sxs-lookup"><span data-stu-id="01990-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01990-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01990-131">Minimum supported client</span></span><br/> | <span data-ttu-id="01990-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01990-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01990-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01990-133">Minimum supported server</span></span><br/> | <span data-ttu-id="01990-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01990-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01990-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="01990-135">End of client support</span></span><br/>    | <span data-ttu-id="01990-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01990-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="01990-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="01990-137">End of server support</span></span><br/>    | <span data-ttu-id="01990-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01990-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="01990-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01990-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="01990-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="01990-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="01990-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="01990-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="01990-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01990-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01990-143">DLL</span><span class="sxs-lookup"><span data-stu-id="01990-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01990-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01990-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01990-145">IID</span><span class="sxs-lookup"><span data-stu-id="01990-145">IID</span></span><br/>                      | <span data-ttu-id="01990-146">IID \_ ISCardTypeConv é definido como 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="01990-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="01990-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="01990-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01990-148">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="01990-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="01990-149">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="01990-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
