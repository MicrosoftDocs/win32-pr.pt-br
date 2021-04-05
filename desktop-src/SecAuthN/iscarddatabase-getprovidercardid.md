---
description: O método GetProviderCardId recupera o identificador (GUID) do provedor de serviços primário para o cartão inteligente especificado.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: 'Método ISCardDatabase:: GetProviderCardId (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f361e83431fa7c6e0a0c2c0ea363bef7e487738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662930"
---
# <a name="iscarddatabasegetprovidercardid-method"></a><span data-ttu-id="7adf3-103">Método ISCardDatabase:: GetProviderCardId</span><span class="sxs-lookup"><span data-stu-id="7adf3-103">ISCardDatabase::GetProviderCardId method</span></span>

<span data-ttu-id="7adf3-104">\[O método **GetProviderCardId** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="7adf3-104">\[The **GetProviderCardId** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7adf3-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7adf3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7adf3-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7adf3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7adf3-107">O método **GetProviderCardId** recupera o identificador (GUID) do [*provedor de serviços primário*](../secgloss/p-gly.md) para o [*cartão inteligente*](../secgloss/s-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="7adf3-107">The **GetProviderCardId** method retrieves the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7adf3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7adf3-108">Syntax</span></span>


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a><span data-ttu-id="7adf3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7adf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adf3-110">*bstrCardName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7adf3-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7adf3-111">Nome do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="7adf3-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="7adf3-112">*ppguidProviderId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7adf3-112">*ppguidProviderId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7adf3-113">Ponteiro para o identificador do provedor de serviços primário (GUID) se for bem-sucedido; **Nulo** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="7adf3-113">Pointer to the primary service provider's identifier (GUID) if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adf3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7adf3-114">Return value</span></span>

<span data-ttu-id="7adf3-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="7adf3-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7adf3-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7adf3-116">Return code</span></span>                                                                                   | <span data-ttu-id="7adf3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7adf3-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="7adf3-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7adf3-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7adf3-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="7adf3-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7adf3-121">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="7adf3-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="7adf3-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7adf3-123">Um ponteiro inadequado foi passado em *ppguidProviderId*.</span><span class="sxs-lookup"><span data-stu-id="7adf3-123">A bad pointer was passed in *ppguidProviderId*.</span></span><br/> |
| <dl> <span data-ttu-id="7adf3-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7adf3-125">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="7adf3-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="7adf3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7adf3-126">Remarks</span></span>

<span data-ttu-id="7adf3-127">Para listar as interfaces do cartão inteligente, chame [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span><span class="sxs-lookup"><span data-stu-id="7adf3-127">To list the interfaces of the smart card, call [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).</span></span>

<span data-ttu-id="7adf3-128">Para recuperar todos os [*cartões inteligentes*](../secgloss/s-gly.md), [*leitores*](../secgloss/r-gly.md) e [*grupos de leitor*](../secgloss/r-gly.md) conhecidos, chame [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7adf3-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md) and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="7adf3-129">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="7adf3-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="7adf3-130">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="7adf3-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7adf3-131">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7adf3-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7adf3-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7adf3-132">Examples</span></span>

<span data-ttu-id="7adf3-133">O exemplo a seguir mostra a recuperação do identificador do provedor de serviços primário para o cartão inteligente especificado.</span><span class="sxs-lookup"><span data-stu-id="7adf3-133">The following example shows retrieving the identifier of the primary service provider for the specified smart card.</span></span>


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="7adf3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7adf3-134">Requirements</span></span>



| <span data-ttu-id="7adf3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adf3-135">Requirement</span></span> | <span data-ttu-id="7adf3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7adf3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adf3-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7adf3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7adf3-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7adf3-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7adf3-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7adf3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7adf3-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7adf3-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7adf3-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7adf3-141">End of client support</span></span><br/>    | <span data-ttu-id="7adf3-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7adf3-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7adf3-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7adf3-143">End of server support</span></span><br/>    | <span data-ttu-id="7adf3-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7adf3-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7adf3-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7adf3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adf3-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7adf3-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7adf3-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="7adf3-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7adf3-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7adf3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adf3-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adf3-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7adf3-151">IID</span><span class="sxs-lookup"><span data-stu-id="7adf3-151">IID</span></span><br/>                      | <span data-ttu-id="7adf3-152">IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7adf3-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7adf3-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="7adf3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adf3-154">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="7adf3-154">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="7adf3-155">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="7adf3-155">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="7adf3-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="7adf3-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="7adf3-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="7adf3-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="7adf3-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="7adf3-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
