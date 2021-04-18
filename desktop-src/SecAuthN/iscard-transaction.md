---
description: Executa uma operação de gravação e leitura no objeto de comando de cartão inteligente (unidade de dados do protocolo de aplicativo).
ms.assetid: 4dc8ed56-97e0-4c05-a70a-ea2ffd976d47
title: 'Método iscard:: Transaction (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Transaction
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2abe9d4acd4d59019fe0c8ce122baa12fde06f2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749970"
---
# <a name="iscardtransaction-method"></a><span data-ttu-id="aac1b-103">Método iscard:: Transaction</span><span class="sxs-lookup"><span data-stu-id="aac1b-103">ISCard::Transaction method</span></span>

<span data-ttu-id="aac1b-104">\[O método de **transação** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="aac1b-104">\[The **Transaction** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aac1b-105">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="aac1b-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="aac1b-106">O método **Transaction** executa uma operação de gravação e leitura no objeto de comando de [*cartão inteligente*](../secgloss/s-gly.md) ([*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="aac1b-106">The **Transaction** method executes a write and read operation on the [*smart card*](../secgloss/s-gly.md) command ([*application protocol data unit*](../secgloss/a-gly.md)) object.</span></span> <span data-ttu-id="aac1b-107">A cadeia de caracteres de resposta do cartão inteligente para a cadeia de caracteres de comando definida no cartão que foi enviado para o cartão inteligente será acessível depois que essa função retornar.</span><span class="sxs-lookup"><span data-stu-id="aac1b-107">The reply string from the smart card for the command string defined in the card that was sent to the smart card will be accessible after this function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac1b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aac1b-108">Syntax</span></span>


```C++
HRESULT Transaction(
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="aac1b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aac1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac1b-110">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="aac1b-110">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aac1b-111">Um ponteiro para o objeto de comando do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="aac1b-111">A pointer to the smart card command object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac1b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aac1b-112">Return value</span></span>

<span data-ttu-id="aac1b-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="aac1b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="aac1b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aac1b-114">Return code</span></span>                                                                                   | <span data-ttu-id="aac1b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="aac1b-115">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="aac1b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aac1b-117">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="aac1b-117">The operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="aac1b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aac1b-119">O parâmetro *ppCmd* não é válido.</span><span class="sxs-lookup"><span data-stu-id="aac1b-119">The *ppCmd* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="aac1b-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aac1b-121">Um ponteiro inadequado foi passado em *ppCmd*.</span><span class="sxs-lookup"><span data-stu-id="aac1b-121">A bad pointer was passed in *ppCmd*.</span></span><br/>          |
| <dl> <span data-ttu-id="aac1b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aac1b-123">A memória para atender à solicitação não está disponível.</span><span class="sxs-lookup"><span data-stu-id="aac1b-123">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aac1b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="aac1b-124">Remarks</span></span>

<span data-ttu-id="aac1b-125">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="aac1b-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="aac1b-126">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="aac1b-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aac1b-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aac1b-127">Examples</span></span>

<span data-ttu-id="aac1b-128">O exemplo a seguir mostra a execução de uma operação de gravação e leitura no objeto de comando do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="aac1b-128">The following example shows executing a write and read operation on the smart card command object.</span></span>


```C++
HRESULT    hr;

// pISCard is a pointer to an instance of ISCard.
// pISCardCmd is a pointer to an instance of ISCardCmd,
// and ISCardCmd::BuildCmd has already been called.
hr = pISCard->Transaction(&pISCardCmd);
if (FAILED(hr))
{
    printf("Failed ISCard::Transaction\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="aac1b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aac1b-129">Requirements</span></span>



| <span data-ttu-id="aac1b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac1b-130">Requirement</span></span> | <span data-ttu-id="aac1b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="aac1b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aac1b-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aac1b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aac1b-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aac1b-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aac1b-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aac1b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aac1b-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aac1b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aac1b-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="aac1b-136">End of client support</span></span><br/>    | <span data-ttu-id="aac1b-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aac1b-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="aac1b-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="aac1b-138">End of server support</span></span><br/>    | <span data-ttu-id="aac1b-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aac1b-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="aac1b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aac1b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac1b-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="aac1b-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aac1b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="aac1b-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aac1b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="aac1b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac1b-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac1b-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aac1b-146">IID</span><span class="sxs-lookup"><span data-stu-id="aac1b-146">IID</span></span><br/>                      | <span data-ttu-id="aac1b-147">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="aac1b-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="aac1b-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="aac1b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aac1b-149">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="aac1b-149">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="aac1b-150">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="aac1b-150">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="aac1b-151">**Detach**</span><span class="sxs-lookup"><span data-stu-id="aac1b-151">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="aac1b-152">**obter \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="aac1b-152">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="aac1b-153">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="aac1b-153">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="aac1b-154">**obter \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="aac1b-154">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="aac1b-155">**obter \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="aac1b-155">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="aac1b-156">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="aac1b-156">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="aac1b-157">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="aac1b-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="aac1b-158">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="aac1b-158">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> <dt>

[<span data-ttu-id="aac1b-159">**Anexar novamente**</span><span class="sxs-lookup"><span data-stu-id="aac1b-159">**ReAttach**</span></span>](iscard-reattach.md)
</dt> <dt>

[<span data-ttu-id="aac1b-160">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="aac1b-160">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
