---
description: Determina o comprimento (em bytes) da unidade de dados do protocolo de aplicativo (APDU).
ms.assetid: 25011db1-a037-4764-b700-8ad2200419da
title: 'Método ISCardCmd:: get_ApduReplyLength (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReplyLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b62e67154ab48f8378c96a78c8bd54765962c3fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171999"
---
# <a name="iscardcmdget_apdureplylength-method"></a><span data-ttu-id="4ba25-103">Método ISCardCmd:: get \_ ApduReplyLength</span><span class="sxs-lookup"><span data-stu-id="4ba25-103">ISCardCmd::get\_ApduReplyLength method</span></span>

<span data-ttu-id="4ba25-104">\[O método **Get \_ ApduReplyLength** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4ba25-104">\[The **get\_ApduReplyLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ba25-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4ba25-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4ba25-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4ba25-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4ba25-107">O método **Get \_ ApduReplyLength** determina o comprimento (em bytes) da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4ba25-107">The **get\_ApduReplyLength** method determines the length (in bytes) of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ba25-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ba25-108">Syntax</span></span>


```C++
HRESULT get_ApduReplyLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="4ba25-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ba25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ba25-110">*plSize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4ba25-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ba25-111">Ponteiro para o tamanho da mensagem de resposta APDU.</span><span class="sxs-lookup"><span data-stu-id="4ba25-111">Pointer to the size of the reply APDU message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ba25-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ba25-112">Return value</span></span>

<span data-ttu-id="4ba25-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4ba25-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4ba25-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4ba25-114">Return code</span></span>                                                                                   | <span data-ttu-id="4ba25-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ba25-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4ba25-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4ba25-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4ba25-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="4ba25-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4ba25-119">O parâmetro *plSize* não é válido.</span><span class="sxs-lookup"><span data-stu-id="4ba25-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4ba25-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4ba25-121">Um ponteiro inadequado foi passado em *plSize*.</span><span class="sxs-lookup"><span data-stu-id="4ba25-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="4ba25-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4ba25-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4ba25-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4ba25-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ba25-124">Remarks</span></span>

<span data-ttu-id="4ba25-125">Para obter um APDU de resposta existente, chame [**Get \_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="4ba25-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4ba25-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4ba25-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4ba25-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4ba25-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ba25-129">Examples</span></span>

<span data-ttu-id="4ba25-130">O exemplo a seguir mostra como recuperar o comprimento do [*APDU de resposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-130">The following example shows how to retrieve the length of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="4ba25-131">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba25-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU reply length.
hr = pISCardCmd->get_ApduReplyLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduReplyLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="4ba25-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ba25-132">Requirements</span></span>



| <span data-ttu-id="4ba25-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ba25-133">Requirement</span></span> | <span data-ttu-id="4ba25-134">Valor</span><span class="sxs-lookup"><span data-stu-id="4ba25-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba25-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ba25-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba25-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4ba25-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4ba25-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ba25-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba25-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4ba25-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4ba25-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4ba25-139">End of client support</span></span><br/>    | <span data-ttu-id="4ba25-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ba25-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4ba25-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4ba25-141">End of server support</span></span><br/>    | <span data-ttu-id="4ba25-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4ba25-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4ba25-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ba25-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba25-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ba25-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ba25-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ba25-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4ba25-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4ba25-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ba25-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ba25-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ba25-149">IID</span><span class="sxs-lookup"><span data-stu-id="4ba25-149">IID</span></span><br/>                      | <span data-ttu-id="4ba25-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4ba25-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4ba25-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ba25-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba25-152">**obter \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="4ba25-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="4ba25-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4ba25-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="4ba25-154">**colocar \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="4ba25-154">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
