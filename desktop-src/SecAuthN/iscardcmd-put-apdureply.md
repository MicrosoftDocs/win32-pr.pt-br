---
description: Define um novo APDU de resposta.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'ISCardCmd: método de ut_ApduReply de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827147"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="30ce5-103">ISCardCmd: método UT \_ ApduReply:p</span><span class="sxs-lookup"><span data-stu-id="30ce5-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="30ce5-104">\[O método **Put \_ ApduReply** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="30ce5-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30ce5-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="30ce5-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30ce5-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="30ce5-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="30ce5-107">O método **Put \_ ApduReply** define um novo [*APDU de resposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="30ce5-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="30ce5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30ce5-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="30ce5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ce5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ce5-110">*pReplyApdu* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30ce5-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ce5-111">Ponteiro para o buffer de bytes (mapeado por meio de um objeto **IStream** ) que contém a mensagem Replay APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="30ce5-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ce5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30ce5-112">Return value</span></span>

<span data-ttu-id="30ce5-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="30ce5-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="30ce5-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30ce5-114">Return code</span></span>                                                                                   | <span data-ttu-id="30ce5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="30ce5-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="30ce5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30ce5-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="30ce5-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="30ce5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="30ce5-119">O parâmetro *pReplyApdu* não é válido.</span><span class="sxs-lookup"><span data-stu-id="30ce5-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="30ce5-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="30ce5-121">Um ponteiro inadequado foi passado em *pReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="30ce5-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="30ce5-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="30ce5-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="30ce5-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="30ce5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="30ce5-124">Remarks</span></span>

<span data-ttu-id="30ce5-125">Para obter um APDU de resposta existente, chame [**Get \_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="30ce5-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="30ce5-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="30ce5-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="30ce5-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="30ce5-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="30ce5-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="30ce5-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="30ce5-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30ce5-129">Examples</span></span>

<span data-ttu-id="30ce5-130">O exemplo a seguir mostra como definir um novo [*APDU de resposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="30ce5-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="30ce5-131">O exemplo supõe que pIByteReply é um ponteiro válido para uma instância de [**IByteBuffer**](ibytebuffer.md)e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="30ce5-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="30ce5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ce5-132">Requirements</span></span>



| <span data-ttu-id="30ce5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ce5-133">Requirement</span></span> | <span data-ttu-id="30ce5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="30ce5-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30ce5-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ce5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="30ce5-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="30ce5-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30ce5-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ce5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="30ce5-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30ce5-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30ce5-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="30ce5-139">End of client support</span></span><br/>    | <span data-ttu-id="30ce5-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30ce5-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="30ce5-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="30ce5-141">End of server support</span></span><br/>    | <span data-ttu-id="30ce5-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30ce5-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="30ce5-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30ce5-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="30ce5-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="30ce5-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="30ce5-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="30ce5-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30ce5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="30ce5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ce5-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30ce5-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="30ce5-149">IID</span><span class="sxs-lookup"><span data-stu-id="30ce5-149">IID</span></span><br/>                      | <span data-ttu-id="30ce5-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="30ce5-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="30ce5-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ce5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ce5-152">**obter \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="30ce5-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="30ce5-153">**obter \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="30ce5-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="30ce5-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="30ce5-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
