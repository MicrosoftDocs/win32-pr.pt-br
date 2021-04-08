---
description: Recupera o identificador de um cartão inteligente conectado. Esse método retornará ( \* pHandle) = = NULL se não estiver conectado.
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'Método iscard:: get_CardHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920684"
---
# <a name="iscardget_cardhandle-method"></a><span data-ttu-id="4a34f-104">Iscard:: obter o \_ método CardHandle</span><span class="sxs-lookup"><span data-stu-id="4a34f-104">ISCard::get\_CardHandle method</span></span>

<span data-ttu-id="4a34f-105">\[O método **Get \_ CardHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4a34f-105">\[The **get\_CardHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a34f-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4a34f-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4a34f-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4a34f-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4a34f-108">O método **Get \_ CardHandle** recupera o identificador de um [*cartão inteligente*](../secgloss/s-gly.md)conectado.</span><span class="sxs-lookup"><span data-stu-id="4a34f-108">The **get\_CardHandle** method retrieves the handle for a connected [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="4a34f-109">Esse método retornará ( \* pHandle) = = **NULL** se não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="4a34f-109">This method returns (\*pHandle) == **NULL** if not connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a34f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a34f-110">Syntax</span></span>


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a><span data-ttu-id="4a34f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a34f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a34f-112">*pHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4a34f-112">*pHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a34f-113">Ponteiro para o identificador do cartão no retorno.</span><span class="sxs-lookup"><span data-stu-id="4a34f-113">Pointer to the card handle on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a34f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a34f-114">Return value</span></span>

<span data-ttu-id="4a34f-115">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4a34f-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4a34f-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4a34f-116">Return code</span></span>                                                                                  | <span data-ttu-id="4a34f-117">Description</span><span class="sxs-lookup"><span data-stu-id="4a34f-117">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="4a34f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="4a34f-119">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4a34f-119">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="4a34f-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="4a34f-121">O parâmetro *pHandle* não é válido.</span><span class="sxs-lookup"><span data-stu-id="4a34f-121">The *pHandle* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4a34f-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-122"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="4a34f-123">Um ponteiro inadequado foi passado em *pHandle*.</span><span class="sxs-lookup"><span data-stu-id="4a34f-123">A bad pointer was passed in *pHandle*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a34f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a34f-124">Remarks</span></span>

<span data-ttu-id="4a34f-125">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4a34f-125">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4a34f-126">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4a34f-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4a34f-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4a34f-127">Examples</span></span>

<span data-ttu-id="4a34f-128">O exemplo a seguir mostra a recuperação da alça do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="4a34f-128">The following example shows retrieving the smart card handle.</span></span>


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
```



## <a name="requirements"></a><span data-ttu-id="4a34f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a34f-129">Requirements</span></span>



| <span data-ttu-id="4a34f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a34f-130">Requirement</span></span> | <span data-ttu-id="4a34f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4a34f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a34f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a34f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4a34f-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4a34f-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4a34f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a34f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4a34f-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a34f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a34f-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4a34f-136">End of client support</span></span><br/>    | <span data-ttu-id="4a34f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a34f-137">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4a34f-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4a34f-138">End of server support</span></span><br/>    | <span data-ttu-id="4a34f-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4a34f-139">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4a34f-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a34f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a34f-141"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-141"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a34f-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4a34f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a34f-143"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-143"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4a34f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4a34f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a34f-145"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a34f-145"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a34f-146">IID</span><span class="sxs-lookup"><span data-stu-id="4a34f-146">IID</span></span><br/>                      | <span data-ttu-id="4a34f-147">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4a34f-147">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4a34f-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a34f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a34f-149">**obter \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="4a34f-149">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="4a34f-150">**obter \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="4a34f-150">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="4a34f-151">**obter \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="4a34f-151">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="4a34f-152">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="4a34f-152">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="4a34f-153">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="4a34f-153">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
