---
description: Libera o acesso exclusivo ao cartão inteligente.
ms.assetid: 12256c91-faf2-4a06-9501-f00d0115a069
title: 'Método iscard:: UnlockSCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.UnlockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 68907e157e60518d1df3855fbca69709f2c21437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661553"
---
# <a name="iscardunlockscard-method"></a><span data-ttu-id="d8f94-103">Método iscard:: UnlockSCard</span><span class="sxs-lookup"><span data-stu-id="d8f94-103">ISCard::UnlockSCard method</span></span>

<span data-ttu-id="d8f94-104">\[O método **UnlockScard** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d8f94-104">\[The **UnlockScard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d8f94-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d8f94-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d8f94-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d8f94-107">O método **UnlockScard** libera acesso exclusivo ao [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d8f94-107">The **UnlockScard** method releases exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f94-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8f94-108">Syntax</span></span>


```C++
HRESULT UnlockSCard(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="d8f94-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8f94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f94-110">*Disposição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f94-111">Indica o que deve ser feito com o cartão no [*leitor*](../secgloss/r-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="d8f94-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="d8f94-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d8f94-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="d8f94-113">Significado</span><span class="sxs-lookup"><span data-stu-id="d8f94-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="d8f94-114"><dt>**Deixe**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="d8f94-115">Deixa o cartão inteligente no [*estado*](../secgloss/s-gly.md)atual.</span><span class="sxs-lookup"><span data-stu-id="d8f94-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="d8f94-116"><dt>**DEFINIDO**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="d8f94-117">Redefine o cartão inteligente para algum estado conhecido.</span><span class="sxs-lookup"><span data-stu-id="d8f94-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="d8f94-118"><dt>**Desligamento**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="d8f94-119">Remove a energia do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="d8f94-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="d8f94-120"><dt>**EJEÇÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="d8f94-121">Ejeta o cartão inteligente se o leitor tiver recursos de ejeção.</span><span class="sxs-lookup"><span data-stu-id="d8f94-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f94-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8f94-122">Return value</span></span>

<span data-ttu-id="d8f94-123">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d8f94-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d8f94-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8f94-124">Return code</span></span>                                                                                  | <span data-ttu-id="d8f94-125">Description</span><span class="sxs-lookup"><span data-stu-id="d8f94-125">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="d8f94-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d8f94-127">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d8f94-127">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="d8f94-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d8f94-129">O parâmetro de *disposição* não é válido</span><span class="sxs-lookup"><span data-stu-id="d8f94-129">The *Disposition* parameter is not valid</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8f94-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8f94-130">Remarks</span></span>

<span data-ttu-id="d8f94-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d8f94-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d8f94-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d8f94-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8f94-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8f94-133">Examples</span></span>

<span data-ttu-id="d8f94-134">O exemplo a seguir mostra a liberação de acesso exclusivo ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="d8f94-134">The following example shows releasing exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Unlock the smart card.
hr = pISCard->UnlockSCard(LEAVE);
if (FAILED(hr))
{
   printf("Failed UnlockSCard\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="d8f94-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8f94-135">Requirements</span></span>



| <span data-ttu-id="d8f94-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8f94-136">Requirement</span></span> | <span data-ttu-id="d8f94-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d8f94-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f94-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f94-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d8f94-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d8f94-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8f94-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d8f94-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d8f94-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d8f94-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d8f94-142">End of client support</span></span><br/>    | <span data-ttu-id="d8f94-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8f94-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d8f94-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d8f94-144">End of server support</span></span><br/>    | <span data-ttu-id="d8f94-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d8f94-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d8f94-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8f94-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8f94-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8f94-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d8f94-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8f94-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d8f94-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d8f94-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8f94-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8f94-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8f94-152">IID</span><span class="sxs-lookup"><span data-stu-id="d8f94-152">IID</span></span><br/>                      | <span data-ttu-id="d8f94-153">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="d8f94-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d8f94-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8f94-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f94-155">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="d8f94-155">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="d8f94-156">**LockSCard**</span><span class="sxs-lookup"><span data-stu-id="d8f94-156">**LockSCard**</span></span>](iscard-lockscard.md)
</dt> </dl>

 

 
