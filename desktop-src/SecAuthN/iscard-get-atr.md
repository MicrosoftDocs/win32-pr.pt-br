---
description: Recupera uma cadeia de caracteres ATR do cartão inteligente.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Método iscard:: get_Atr (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748960"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="b4fed-103">Método de @ card:: obter \_ ATR</span><span class="sxs-lookup"><span data-stu-id="b4fed-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="b4fed-104">\[O método **obter \_ ATR** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b4fed-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4fed-105">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b4fed-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b4fed-106">O método **Get \_ ATR** recupera uma [*cadeia de caracteres ATR*](../secgloss/a-gly.md) do [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b4fed-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4fed-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="b4fed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4fed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fed-109">*ppAtr* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b4fed-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4fed-110">Ponteiro para um buffer de bytes na forma de um [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) que conterá a cadeia de caracteres ATR no retorno.</span><span class="sxs-lookup"><span data-stu-id="b4fed-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4fed-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4fed-111">Return value</span></span>

<span data-ttu-id="b4fed-112">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b4fed-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b4fed-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b4fed-113">Return code</span></span>                                                                                   | <span data-ttu-id="b4fed-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4fed-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="b4fed-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b4fed-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b4fed-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="b4fed-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b4fed-118">O parâmetro *ppAtr* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b4fed-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="b4fed-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b4fed-120">Um ponteiro inadequado foi passado em *ppAtr*.</span><span class="sxs-lookup"><span data-stu-id="b4fed-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="b4fed-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b4fed-122">A memória para atender à solicitação não está disponível.</span><span class="sxs-lookup"><span data-stu-id="b4fed-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4fed-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4fed-123">Remarks</span></span>

<span data-ttu-id="b4fed-124">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4fed-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b4fed-125">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b4fed-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b4fed-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4fed-126">Examples</span></span>

<span data-ttu-id="b4fed-127">O exemplo a seguir mostra a recuperação da cadeia de caracteres ATR do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="b4fed-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="b4fed-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4fed-128">Requirements</span></span>



| <span data-ttu-id="b4fed-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4fed-129">Requirement</span></span> | <span data-ttu-id="b4fed-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b4fed-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fed-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4fed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fed-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4fed-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b4fed-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4fed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fed-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4fed-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4fed-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b4fed-135">End of client support</span></span><br/>    | <span data-ttu-id="b4fed-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4fed-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b4fed-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b4fed-137">End of server support</span></span><br/>    | <span data-ttu-id="b4fed-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4fed-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b4fed-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4fed-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4fed-140"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4fed-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4fed-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4fed-142"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4fed-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b4fed-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4fed-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4fed-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b4fed-145">IID</span><span class="sxs-lookup"><span data-stu-id="b4fed-145">IID</span></span><br/>                      | <span data-ttu-id="b4fed-146">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b4fed-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b4fed-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4fed-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fed-148">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="b4fed-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="b4fed-149">**obter \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="b4fed-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="b4fed-150">**obter \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="b4fed-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="b4fed-151">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="b4fed-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="b4fed-152">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="b4fed-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="b4fed-153">**IByteBuffer:: ler**</span><span class="sxs-lookup"><span data-stu-id="b4fed-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
