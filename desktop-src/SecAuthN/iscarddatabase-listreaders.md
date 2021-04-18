---
description: O método ListReaders recupera os nomes dos leitores de cartão inteligente registrados no banco de dados do cartão inteligente.
ms.assetid: e1ca85a1-9206-4c09-ba0f-10b60e472dfb
title: 'Método ISCardDatabase:: ListReaders (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaders
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dcd78066a95c69b75d5089ba1683e5c937cb7414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752015"
---
# <a name="iscarddatabaselistreaders-method"></a><span data-ttu-id="6e25c-103">Método ISCardDatabase:: ListReaders</span><span class="sxs-lookup"><span data-stu-id="6e25c-103">ISCardDatabase::ListReaders method</span></span>

<span data-ttu-id="6e25c-104">\[O método **ListReaders** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6e25c-104">\[The **ListReaders** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6e25c-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6e25c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6e25c-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="6e25c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6e25c-107">O método **ListReaders** recupera os nomes dos [*leitores*](../secgloss/r-gly.md) de cartão inteligente registrados no banco de [*dados do cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6e25c-107">The **ListReaders** method retrieves the names of the smart card [*readers*](../secgloss/r-gly.md) registered in the [*smart card database*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e25c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e25c-108">Syntax</span></span>


```C++
HRESULT ListReaders(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaders
);
```



## <a name="parameters"></a><span data-ttu-id="6e25c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e25c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e25c-110">*LocaleID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e25c-110">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e25c-111">ID da localização do idioma.</span><span class="sxs-lookup"><span data-stu-id="6e25c-111">Language localization ID.</span></span>

</dd> <dt>

<span data-ttu-id="6e25c-112">*ppReaders* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e25c-112">*ppReaders* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e25c-113">Ponteiro para um SAFEARRAY de BSTRs que contém os nomes dos leitores de cartão inteligente, se for bem-sucedido; **NULL** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="6e25c-113">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart card readers if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e25c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e25c-114">Return value</span></span>

<span data-ttu-id="6e25c-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="6e25c-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6e25c-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6e25c-116">Return code</span></span>                                                                                   | <span data-ttu-id="6e25c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e25c-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="6e25c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6e25c-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6e25c-119">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="6e25c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6e25c-121">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="6e25c-121">Invalid parameter.</span></span><br/>                       |
| <dl> <span data-ttu-id="6e25c-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6e25c-123">Um ponteiro inadequado foi passado em *ppReaders*.</span><span class="sxs-lookup"><span data-stu-id="6e25c-123">A bad pointer was passed in *ppReaders*.</span></span><br/> |
| <dl> <span data-ttu-id="6e25c-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6e25c-125">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="6e25c-125">Out of memory.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="6e25c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e25c-126">Remarks</span></span>

<span data-ttu-id="6e25c-127">Para recuperar todos os [*cartões inteligentes*](../secgloss/s-gly.md) ou [*grupos de leitores*](../secgloss/r-gly.md)conhecidos, chame [**ListCards**](iscarddatabase-listcards.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6e25c-127">To retrieve all known [*smart cards*](../secgloss/s-gly.md) or [*reader groups*](../secgloss/r-gly.md), call [**ListCards**](iscarddatabase-listcards.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="6e25c-128">Para recuperar o [*provedor de serviços primário*](../secgloss/p-gly.md) ou as interfaces de um cartão específico [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6e25c-128">To retrieve the [*primary service provider*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="6e25c-129">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="6e25c-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="6e25c-130">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="6e25c-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6e25c-131">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6e25c-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6e25c-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e25c-132">Examples</span></span>

<span data-ttu-id="6e25c-133">O exemplo a seguir mostra a recuperação dos nomes dos leitores de cartão inteligente registrados no banco de dados do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="6e25c-133">The following example shows retrieving the names of the smart card readers registered in the smart card database.</span></span>


```C++
LPSAFEARRAY pReaders = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaders(0x0409,  // English (US)
                               &pReaders);
if (FAILED(hr))
{
   printf("Failed ListReaders\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
}
```



## <a name="requirements"></a><span data-ttu-id="6e25c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e25c-134">Requirements</span></span>



| <span data-ttu-id="6e25c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e25c-135">Requirement</span></span> | <span data-ttu-id="6e25c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="6e25c-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e25c-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e25c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6e25c-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e25c-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e25c-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e25c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6e25c-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e25c-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e25c-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6e25c-141">End of client support</span></span><br/>    | <span data-ttu-id="6e25c-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e25c-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6e25c-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6e25c-143">End of server support</span></span><br/>    | <span data-ttu-id="6e25c-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6e25c-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6e25c-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e25c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e25c-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e25c-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e25c-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e25c-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6e25c-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6e25c-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e25c-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e25c-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e25c-151">IID</span><span class="sxs-lookup"><span data-stu-id="6e25c-151">IID</span></span><br/>                      | <span data-ttu-id="6e25c-152">IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6e25c-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6e25c-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e25c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e25c-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="6e25c-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="6e25c-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="6e25c-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="6e25c-156">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="6e25c-156">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="6e25c-157">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="6e25c-157">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="6e25c-158">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="6e25c-158">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> </dl>

 

 
