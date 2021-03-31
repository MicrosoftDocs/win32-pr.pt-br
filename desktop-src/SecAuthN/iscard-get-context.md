---
description: Recupera o identificador de contexto atual do Resource Manager. Esse método retornará ( \* pContext) = = NULL se nenhum contexto tiver sido estabelecido.
ms.assetid: c031f53d-4670-4d48-934c-a1550f21c23a
title: 'Método iscard:: get_Context (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Context
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8b5aba075d755b644a78cca23a827a70966f4ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829755"
---
# <a name="iscardget_context-method"></a><span data-ttu-id="2c1ea-104">Método de contexto iscard:: get \_</span><span class="sxs-lookup"><span data-stu-id="2c1ea-104">ISCard::get\_Context method</span></span>

<span data-ttu-id="2c1ea-105">\[O método de **\_ contexto Get** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-105">\[The **get\_Context** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c1ea-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c1ea-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2c1ea-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2c1ea-108">O método de **\_ contexto Get** recupera o identificador de contexto atual do [*Resource Manager*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2c1ea-108">The **get\_Context** method retrieves the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span> <span data-ttu-id="2c1ea-109">Esse método retornará ( \* *pContext*) = = **NULL** se nenhum contexto tiver sido estabelecido.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-109">This method returns (\**pContext*) == **NULL** if no context has been established.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1ea-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c1ea-110">Syntax</span></span>


```C++
HRESULT get_Context(
  [out] HSCARDCONTEXT *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="2c1ea-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c1ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c1ea-112">*pContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c1ea-112">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c1ea-113">Ponteiro para o identificador de contexto no retorno.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-113">Pointer to the context handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c1ea-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c1ea-114">Return value</span></span>

<span data-ttu-id="2c1ea-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2c1ea-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2c1ea-116">Return code</span></span>                                                                                  | <span data-ttu-id="2c1ea-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c1ea-117">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="2c1ea-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2c1ea-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-119">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="2c1ea-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2c1ea-121">O parâmetro *pContext* não é válido.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-121">The *pContext* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="2c1ea-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="2c1ea-123">Um ponteiro inadequado foi passado em *pContext*.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-123">A bad pointer was passed in *pContext*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c1ea-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c1ea-124">Remarks</span></span>

<span data-ttu-id="2c1ea-125">O contexto do Gerenciador de recursos é definido chamando a função de [*cartão inteligente*](../secgloss/s-gly.md) [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span><span class="sxs-lookup"><span data-stu-id="2c1ea-125">The resource manager context is set by calling the [*smart card*](../secgloss/s-gly.md) function [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext).</span></span>

<span data-ttu-id="2c1ea-126">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-126">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2c1ea-127">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2c1ea-127">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2c1ea-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c1ea-128">Examples</span></span>

<span data-ttu-id="2c1ea-129">O exemplo a seguir mostra a recuperação do identificador de [*contexto do Resource Manager*](../secgloss/r-gly.md) atual.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-129">The following example shows retrieving the current [*resource manager context*](../secgloss/r-gly.md) handle.</span></span>


```C++
HSCARDCONTEXT  hCtx;
HRESULT        hr;

// Retrieve the smart card context.
hr = pISCard->get_Context(&hCtx);
if (FAILED(hr))
{
   printf("Failed get_Context\n");
   // Take other error handling action as needed.
}
// Use smart card context as needed.
```



## <a name="requirements"></a><span data-ttu-id="2c1ea-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c1ea-130">Requirements</span></span>



| <span data-ttu-id="2c1ea-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c1ea-131">Requirement</span></span> | <span data-ttu-id="2c1ea-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2c1ea-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1ea-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c1ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1ea-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2c1ea-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c1ea-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c1ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1ea-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c1ea-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c1ea-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2c1ea-137">End of client support</span></span><br/>    | <span data-ttu-id="2c1ea-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c1ea-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2c1ea-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2c1ea-139">End of server support</span></span><br/>    | <span data-ttu-id="2c1ea-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c1ea-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2c1ea-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c1ea-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c1ea-142"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-142"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c1ea-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2c1ea-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c1ea-144"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-144"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c1ea-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2c1ea-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c1ea-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c1ea-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c1ea-147">IID</span><span class="sxs-lookup"><span data-stu-id="2c1ea-147">IID</span></span><br/>                      | <span data-ttu-id="2c1ea-148">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="2c1ea-148">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2c1ea-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c1ea-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1ea-150">**obter \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-150">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="2c1ea-151">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-151">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="2c1ea-152">**obter \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-152">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="2c1ea-153">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-153">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="2c1ea-154">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-154">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="2c1ea-155">**SCardEstablishContext**</span><span class="sxs-lookup"><span data-stu-id="2c1ea-155">**SCardEstablishContext**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext)
</dt> </dl>

 

 
