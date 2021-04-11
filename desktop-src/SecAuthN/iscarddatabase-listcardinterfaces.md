---
description: O método ListCardInterfaces recupera os identificadores (GUIDs) de todas as interfaces com suporte para o cartão inteligente especificado.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Método ISCardDatabase:: ListCardInterfaces (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164283"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="49daf-103">Método ISCardDatabase:: ListCardInterfaces</span><span class="sxs-lookup"><span data-stu-id="49daf-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="49daf-104">\[O método **ListCardInterfaces** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="49daf-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="49daf-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="49daf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="49daf-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="49daf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="49daf-107">O método **ListCardInterfaces** recupera os identificadores (GUIDs) de todas as interfaces com suporte para o [*cartão inteligente*](../secgloss/s-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="49daf-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49daf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49daf-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="49daf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49daf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49daf-110">*bstrCardName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="49daf-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49daf-111">Nome do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="49daf-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="49daf-112">*ppInterfaceGuids* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="49daf-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49daf-113">Ponteiro para os GUIDs de interface se for bem-sucedido; **Nulo** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="49daf-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49daf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49daf-114">Return value</span></span>

<span data-ttu-id="49daf-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="49daf-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="49daf-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="49daf-116">Return code</span></span>                                                                                   | <span data-ttu-id="49daf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="49daf-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="49daf-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="49daf-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="49daf-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="49daf-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="49daf-121">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="49daf-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="49daf-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="49daf-123">Um ponteiro inadequado foi passado em *ppInterfaceGuids*.</span><span class="sxs-lookup"><span data-stu-id="49daf-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="49daf-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="49daf-125">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="49daf-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="49daf-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="49daf-126">Remarks</span></span>

<span data-ttu-id="49daf-127">Para recuperar o [*provedor de serviços primário*](../secgloss/p-gly.md) do cartão inteligente, chame [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span><span class="sxs-lookup"><span data-stu-id="49daf-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="49daf-128">Para recuperar todos os [*cartões inteligentes*](../secgloss/s-gly.md), [*leitores*](../secgloss/r-gly.md)e [*grupos*](../secgloss/r-gly.md) de leitores conhecidos, chame [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="49daf-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="49daf-129">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="49daf-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="49daf-130">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="49daf-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="49daf-131">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="49daf-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="49daf-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49daf-132">Examples</span></span>

<span data-ttu-id="49daf-133">O exemplo a seguir mostra a recuperação dos identificadores das interfaces com suporte para o cartão inteligente especificado.</span><span class="sxs-lookup"><span data-stu-id="49daf-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="49daf-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49daf-134">Requirements</span></span>



| <span data-ttu-id="49daf-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="49daf-135">Requirement</span></span> | <span data-ttu-id="49daf-136">Valor</span><span class="sxs-lookup"><span data-stu-id="49daf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49daf-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49daf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="49daf-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49daf-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="49daf-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49daf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="49daf-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49daf-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49daf-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="49daf-141">End of client support</span></span><br/>    | <span data-ttu-id="49daf-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="49daf-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="49daf-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="49daf-143">End of server support</span></span><br/>    | <span data-ttu-id="49daf-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49daf-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="49daf-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49daf-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="49daf-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="49daf-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="49daf-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="49daf-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49daf-149">DLL</span><span class="sxs-lookup"><span data-stu-id="49daf-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49daf-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49daf-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49daf-151">IID</span><span class="sxs-lookup"><span data-stu-id="49daf-151">IID</span></span><br/>                      | <span data-ttu-id="49daf-152">IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="49daf-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="49daf-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="49daf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49daf-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="49daf-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="49daf-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="49daf-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="49daf-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="49daf-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="49daf-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="49daf-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="49daf-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="49daf-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
