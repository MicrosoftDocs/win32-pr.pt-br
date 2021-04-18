---
description: Fecha a conexão aberta com o cartão inteligente.
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: Iscard::D método Etach (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751526"
---
# <a name="iscarddetach-method"></a><span data-ttu-id="11fee-103">Iscard::D método Etach</span><span class="sxs-lookup"><span data-stu-id="11fee-103">ISCard::Detach method</span></span>

<span data-ttu-id="11fee-104">\[O método **Detach** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="11fee-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="11fee-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="11fee-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11fee-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="11fee-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="11fee-107">O método **Detach** fecha a conexão aberta com o [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="11fee-107">The **Detach** method closes the open connection to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="11fee-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11fee-108">Syntax</span></span>


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="11fee-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11fee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11fee-110">*Disposição* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="11fee-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11fee-111">Indica o que deve ser feito com o cartão no [*leitor*](../secgloss/r-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="11fee-111">Indicates what should be done with the card in the connected [*reader*](../secgloss/r-gly.md).</span></span>



| <span data-ttu-id="11fee-112">Valor</span><span class="sxs-lookup"><span data-stu-id="11fee-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="11fee-113">Significado</span><span class="sxs-lookup"><span data-stu-id="11fee-113">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="11fee-114"><dt>**Deixe**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-114"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="11fee-115">Deixa o cartão inteligente no [*estado*](../secgloss/s-gly.md)atual.</span><span class="sxs-lookup"><span data-stu-id="11fee-115">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="11fee-116"><dt>**DEFINIDO**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-116"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="11fee-117">Redefine o cartão inteligente para algum estado conhecido.</span><span class="sxs-lookup"><span data-stu-id="11fee-117">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="11fee-118"><dt>**Desligamento**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-118"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="11fee-119">Remove a energia do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="11fee-119">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="11fee-120"><dt>**EJEÇÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-120"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="11fee-121">Ejeta o cartão inteligente se o leitor tiver recursos de ejeção.</span><span class="sxs-lookup"><span data-stu-id="11fee-121">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11fee-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11fee-122">Return value</span></span>

<span data-ttu-id="11fee-123">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="11fee-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="11fee-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="11fee-124">Return code</span></span>                                                                                  | <span data-ttu-id="11fee-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="11fee-125">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="11fee-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="11fee-127">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="11fee-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="11fee-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="11fee-129">A *disposição* não é válida.</span><span class="sxs-lookup"><span data-stu-id="11fee-129">*Disposition* is not valid.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="11fee-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="11fee-130">Remarks</span></span>

<span data-ttu-id="11fee-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="11fee-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="11fee-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="11fee-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="11fee-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11fee-133">Examples</span></span>

<span data-ttu-id="11fee-134">O exemplo a seguir mostra como fechar a conexão com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="11fee-134">The following example shows closing the connection to the smart card.</span></span>


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="11fee-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11fee-135">Requirements</span></span>



| <span data-ttu-id="11fee-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="11fee-136">Requirement</span></span> | <span data-ttu-id="11fee-137">Valor</span><span class="sxs-lookup"><span data-stu-id="11fee-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11fee-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11fee-138">Minimum supported client</span></span><br/> | <span data-ttu-id="11fee-139">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="11fee-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="11fee-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11fee-140">Minimum supported server</span></span><br/> | <span data-ttu-id="11fee-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11fee-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11fee-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="11fee-142">End of client support</span></span><br/>    | <span data-ttu-id="11fee-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11fee-143">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="11fee-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="11fee-144">End of server support</span></span><br/>    | <span data-ttu-id="11fee-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11fee-145">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="11fee-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11fee-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="11fee-147"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-147"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="11fee-148">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="11fee-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="11fee-149"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-149"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11fee-150">DLL</span><span class="sxs-lookup"><span data-stu-id="11fee-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11fee-151"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11fee-151"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="11fee-152">IID</span><span class="sxs-lookup"><span data-stu-id="11fee-152">IID</span></span><br/>                      | <span data-ttu-id="11fee-153">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="11fee-153">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="11fee-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="11fee-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11fee-155">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="11fee-155">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="11fee-156">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="11fee-156">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="11fee-157">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="11fee-157">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="11fee-158">**Anexar novamente**</span><span class="sxs-lookup"><span data-stu-id="11fee-158">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
