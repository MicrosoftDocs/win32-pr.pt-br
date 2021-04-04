---
description: O método ListCards recupera todos os nomes de cartão inteligente que correspondem aos GUIDs (identificadores de interface) especificados, à cadeia de caracteres ATR especificada ou a ambos.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Método ISCardDatabase:: ListCards (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647195"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="82dc1-103">Método ISCardDatabase:: ListCards</span><span class="sxs-lookup"><span data-stu-id="82dc1-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="82dc1-104">\[O método **ListCards** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="82dc1-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="82dc1-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="82dc1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="82dc1-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="82dc1-107">O método **ListCards** recupera todos os nomes de cartão inteligente que correspondem aos GUIDs (identificadores de interface) especificados, à [*cadeia de caracteres ATR*](../secgloss/a-gly.md)especificada ou a ambos.</span><span class="sxs-lookup"><span data-stu-id="82dc1-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="82dc1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82dc1-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="82dc1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82dc1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82dc1-110">*pAtr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82dc1-111">Ponteiro para uma cadeia de caracteres ATR de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="82dc1-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="82dc1-112">A cadeia de caracteres ATR deve ser empacotada em um [**IByteBuffer**](ibytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="82dc1-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="82dc1-113">*pInterfaceGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82dc1-114">Ponteiro para um SAFEARRAY de identificadores de interface COM (GUIDs) no formato BSTR.</span><span class="sxs-lookup"><span data-stu-id="82dc1-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="82dc1-115">*LocaleID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82dc1-116">Identificador de localização de idioma.</span><span class="sxs-lookup"><span data-stu-id="82dc1-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="82dc1-117">*ppCardNames* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82dc1-118">Ponteiro para uma SAFEARRAY de BSTRs que contém os nomes dos cartões inteligentes que atenderam aos parâmetros de pesquisa se bem-sucedidos; **NULL** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="82dc1-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82dc1-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82dc1-119">Return value</span></span>

<span data-ttu-id="82dc1-120">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="82dc1-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="82dc1-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="82dc1-121">Return code</span></span>                                                                                   | <span data-ttu-id="82dc1-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="82dc1-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="82dc1-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82dc1-124">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="82dc1-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="82dc1-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="82dc1-126">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="82dc1-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="82dc1-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="82dc1-128">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="82dc1-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="82dc1-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82dc1-130">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="82dc1-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="82dc1-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="82dc1-131">Remarks</span></span>

<span data-ttu-id="82dc1-132">Para recuperar todos os [*leitores*](../secgloss/r-gly.md) ou [*leitor*](../secgloss/r-gly.md)conhecidos, chame [**ListReaders**](iscarddatabase-listreaders.md) ou [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="82dc1-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="82dc1-133">Para recuperar o [*serviço primário*](../secgloss/p-gly.md) ou as interfaces de um cartão específico [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) ou [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="82dc1-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="82dc1-134">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="82dc1-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="82dc1-135">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="82dc1-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="82dc1-136">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="82dc1-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="82dc1-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82dc1-137">Examples</span></span>

<span data-ttu-id="82dc1-138">O exemplo a seguir mostra a recuperação de nomes de cartão inteligente que correspondem à cadeia de caracteres ATR especificada.</span><span class="sxs-lookup"><span data-stu-id="82dc1-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="82dc1-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82dc1-139">Requirements</span></span>



| <span data-ttu-id="82dc1-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="82dc1-140">Requirement</span></span> | <span data-ttu-id="82dc1-141">Valor</span><span class="sxs-lookup"><span data-stu-id="82dc1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82dc1-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82dc1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="82dc1-143">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="82dc1-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82dc1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="82dc1-145">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82dc1-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82dc1-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="82dc1-146">End of client support</span></span><br/>    | <span data-ttu-id="82dc1-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="82dc1-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="82dc1-148">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="82dc1-148">End of server support</span></span><br/>    | <span data-ttu-id="82dc1-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="82dc1-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="82dc1-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82dc1-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="82dc1-151"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="82dc1-152">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="82dc1-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="82dc1-153"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82dc1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="82dc1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82dc1-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82dc1-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="82dc1-156">IID</span><span class="sxs-lookup"><span data-stu-id="82dc1-156">IID</span></span><br/>                      | <span data-ttu-id="82dc1-157">IID \_ ISCardDatabase é definido como 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="82dc1-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="82dc1-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="82dc1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82dc1-159">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="82dc1-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="82dc1-160">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="82dc1-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="82dc1-161">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="82dc1-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="82dc1-162">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="82dc1-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="82dc1-163">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="82dc1-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
