---
description: O método GetResponse constrói um comando APDU (unidade de dados de protocolo de aplicativo) que transmite comandos APDU (ou parte de um comando APDU) que, de outra forma, não podiam ser transmitidos pelos protocolos disponíveis.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'Método ISCardISO7816:: GetResponse (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750201"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="c9688-103">Método ISCardISO7816:: GetResponse</span><span class="sxs-lookup"><span data-stu-id="c9688-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="c9688-104">\[O método **GetResponse** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c9688-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c9688-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c9688-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c9688-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c9688-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c9688-107">O método **GetResponse** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que transmite comandos APDU (ou parte de um comando APDU) que, de outra forma, não podiam ser transmitidos pelos protocolos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c9688-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9688-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9688-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="c9688-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9688-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9688-110">*byP1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9688-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9688-111">De acordo com o ISO 7816-4, P1 deve ser zero (RFU).</span><span class="sxs-lookup"><span data-stu-id="c9688-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="c9688-112">*byP2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9688-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9688-113">De acordo com o ISO 7816-4, P2 deve ser zero (RFU).</span><span class="sxs-lookup"><span data-stu-id="c9688-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="c9688-114">*lDataLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c9688-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9688-115">Comprimento dos dados transmitidos.</span><span class="sxs-lookup"><span data-stu-id="c9688-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="c9688-116">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c9688-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9688-117">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c9688-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="c9688-118">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="c9688-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="c9688-119">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="c9688-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9688-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c9688-120">Return value</span></span>

<span data-ttu-id="c9688-121">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c9688-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c9688-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c9688-122">Return code</span></span>                                                                                   | <span data-ttu-id="c9688-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9688-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c9688-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c9688-125">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c9688-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="c9688-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c9688-127">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="c9688-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="c9688-128"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c9688-129">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="c9688-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="c9688-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c9688-131">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c9688-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="c9688-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9688-132">Remarks</span></span>

<span data-ttu-id="c9688-133">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="c9688-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="c9688-134">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c9688-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c9688-135">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c9688-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9688-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9688-136">Requirements</span></span>



| <span data-ttu-id="c9688-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9688-137">Requirement</span></span> | <span data-ttu-id="c9688-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c9688-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9688-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9688-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c9688-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9688-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9688-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9688-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c9688-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9688-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c9688-143">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c9688-143">End of client support</span></span><br/>    | <span data-ttu-id="c9688-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c9688-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c9688-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c9688-145">End of server support</span></span><br/>    | <span data-ttu-id="c9688-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c9688-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c9688-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9688-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9688-148"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9688-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c9688-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="c9688-150"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c9688-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c9688-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9688-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9688-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9688-153">IID</span><span class="sxs-lookup"><span data-stu-id="c9688-153">IID</span></span><br/>                      | <span data-ttu-id="c9688-154">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c9688-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c9688-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9688-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9688-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="c9688-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
