---
description: O método de reanexação redefine ou reinicializa o cartão inteligente.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'Método iscard:: reattach (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164988"
---
# <a name="iscardreattach-method"></a><span data-ttu-id="4de5b-103">Método iscard:: reattach</span><span class="sxs-lookup"><span data-stu-id="4de5b-103">ISCard::ReAttach method</span></span>

<span data-ttu-id="4de5b-104">\[O método de **reanexação** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4de5b-104">\[The **ReAttach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4de5b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4de5b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4de5b-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4de5b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4de5b-107">O método de **reanexação** redefine ou reinicializa o [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4de5b-107">The **ReAttach** method resets, or reinitializes, the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4de5b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4de5b-108">Syntax</span></span>


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a><span data-ttu-id="4de5b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4de5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de5b-110">*ShareMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4de5b-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de5b-111">Modo no qual compartilhar ou possuir exclusivamente a conexão com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4de5b-111">Mode in which to share or exclusively own the connection to the smart card.</span></span>



| <span data-ttu-id="4de5b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4de5b-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="4de5b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4de5b-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="4de5b-114"><dt>**Exclude**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="4de5b-115">Ninguém mais usa essa conexão com o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4de5b-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="4de5b-116"><dt>**COMPARTILHADO**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="4de5b-117">Outros aplicativos podem usar essa conexão.</span><span class="sxs-lookup"><span data-stu-id="4de5b-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="4de5b-118">*Initstate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4de5b-118">*InitState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de5b-119">Indica o que fazer com o cartão.</span><span class="sxs-lookup"><span data-stu-id="4de5b-119">Indicates what to do with the card.</span></span>



| <span data-ttu-id="4de5b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4de5b-120">Value</span></span>                                                                                                                                      | <span data-ttu-id="4de5b-121">Significado</span><span class="sxs-lookup"><span data-stu-id="4de5b-121">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <span data-ttu-id="4de5b-122"><dt>**Deixe**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-122"><dt>**LEAVE**</dt></span></span> </dl>       | <span data-ttu-id="4de5b-123">Deixa o cartão inteligente no [*estado*](../secgloss/s-gly.md)atual.</span><span class="sxs-lookup"><span data-stu-id="4de5b-123">Leaves the smart card in the current [*state*](../secgloss/s-gly.md).</span></span><br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <span data-ttu-id="4de5b-124"><dt>**DEFINIDO**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-124"><dt>**RESET**</dt></span></span> </dl>       | <span data-ttu-id="4de5b-125">Redefine o cartão inteligente para algum estado conhecido.</span><span class="sxs-lookup"><span data-stu-id="4de5b-125">Resets the smart card to some known state.</span></span><br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <span data-ttu-id="4de5b-126"><dt>**Desligamento**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-126"><dt>**UNPOWER**</dt></span></span> </dl> | <span data-ttu-id="4de5b-127">Remove a energia do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4de5b-127">Removes power from the smart card.</span></span><br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <span data-ttu-id="4de5b-128"><dt>**EJEÇÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-128"><dt>**EJECT**</dt></span></span> </dl>       | <span data-ttu-id="4de5b-129">Ejeta o cartão inteligente se o leitor tiver recursos de ejeção.</span><span class="sxs-lookup"><span data-stu-id="4de5b-129">Ejects the smart card if the reader has eject capabilities.</span></span><br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4de5b-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4de5b-130">Return value</span></span>

<span data-ttu-id="4de5b-131">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4de5b-131">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4de5b-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4de5b-132">Return code</span></span>                                                                                  | <span data-ttu-id="4de5b-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="4de5b-133">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4de5b-134"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-134"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4de5b-135">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4de5b-135">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4de5b-136"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-136"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4de5b-137">Há algo errado com um ou mais dos parâmetros passados para a função.</span><span class="sxs-lookup"><span data-stu-id="4de5b-137">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4de5b-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="4de5b-138">Remarks</span></span>

<span data-ttu-id="4de5b-139">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4de5b-139">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4de5b-140">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4de5b-140">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4de5b-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4de5b-141">Examples</span></span>

<span data-ttu-id="4de5b-142">O exemplo a seguir mostra a reinicialização do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4de5b-142">The following example shows reinitializing the smart card.</span></span>


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="4de5b-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4de5b-143">Requirements</span></span>



| <span data-ttu-id="4de5b-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de5b-144">Requirement</span></span> | <span data-ttu-id="4de5b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="4de5b-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de5b-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4de5b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4de5b-147">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4de5b-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4de5b-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4de5b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4de5b-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4de5b-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4de5b-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4de5b-150">End of client support</span></span><br/>    | <span data-ttu-id="4de5b-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4de5b-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4de5b-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4de5b-152">End of server support</span></span><br/>    | <span data-ttu-id="4de5b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4de5b-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4de5b-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4de5b-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="4de5b-155"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-155"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="4de5b-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4de5b-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="4de5b-157"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-157"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4de5b-158">DLL</span><span class="sxs-lookup"><span data-stu-id="4de5b-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de5b-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de5b-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4de5b-160">IID</span><span class="sxs-lookup"><span data-stu-id="4de5b-160">IID</span></span><br/>                      | <span data-ttu-id="4de5b-161">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4de5b-161">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4de5b-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="4de5b-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de5b-163">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="4de5b-163">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="4de5b-164">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="4de5b-164">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="4de5b-165">**Detach**</span><span class="sxs-lookup"><span data-stu-id="4de5b-165">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="4de5b-166">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="4de5b-166">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
