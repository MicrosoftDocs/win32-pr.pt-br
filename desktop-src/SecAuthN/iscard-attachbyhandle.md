---
description: Anexa o objeto iscard a um identificador de cartão inteligente aberto e configurado.
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'Método iscard:: AttachByHandle (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749686"
---
# <a name="iscardattachbyhandle-method"></a><span data-ttu-id="dd14e-103">Método iscard:: AttachByHandle</span><span class="sxs-lookup"><span data-stu-id="dd14e-103">ISCard::AttachByHandle method</span></span>

<span data-ttu-id="dd14e-104">\[O método **AttachByHandle** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="dd14e-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd14e-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd14e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd14e-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="dd14e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dd14e-107">O método **AttachByHandle** anexa o objeto [**iscard**](iscard.md) a um identificador de [*cartão inteligente*](../secgloss/s-gly.md) aberto e configurado.</span><span class="sxs-lookup"><span data-stu-id="dd14e-107">The **AttachByHandle** method attaches the [**ISCard**](iscard.md) object to an open and configured [*smart card*](../secgloss/s-gly.md) handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd14e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd14e-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a><span data-ttu-id="dd14e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd14e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd14e-110">*hCard* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dd14e-110">*hCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd14e-111">Um identificador para uma conexão aberta com um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="dd14e-111">A handle to an open connection to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd14e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd14e-112">Return value</span></span>

<span data-ttu-id="dd14e-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="dd14e-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dd14e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dd14e-114">Return code</span></span>                                                                                  | <span data-ttu-id="dd14e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd14e-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="dd14e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd14e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dd14e-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="dd14e-117">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="dd14e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd14e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dd14e-119">O parâmetro *hCard* não é válido.</span><span class="sxs-lookup"><span data-stu-id="dd14e-119">The *hCard* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dd14e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd14e-120">Remarks</span></span>

<span data-ttu-id="dd14e-121">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="dd14e-121">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dd14e-122">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dd14e-122">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="dd14e-123">Quando terminar de usar o identificador, libere o anexo chamando o método [**iscard::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="dd14e-123">When you have finished using the handle, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="dd14e-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dd14e-124">Examples</span></span>

<span data-ttu-id="dd14e-125">O exemplo a seguir mostra a anexação a um identificador de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="dd14e-125">The following example shows attaching to a smart card handle.</span></span>


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
```



## <a name="requirements"></a><span data-ttu-id="dd14e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd14e-126">Requirements</span></span>



| <span data-ttu-id="dd14e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd14e-127">Requirement</span></span> | <span data-ttu-id="dd14e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dd14e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd14e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd14e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd14e-130">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd14e-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd14e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd14e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd14e-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd14e-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd14e-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dd14e-133">End of client support</span></span><br/>    | <span data-ttu-id="dd14e-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd14e-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dd14e-135">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="dd14e-135">End of server support</span></span><br/>    | <span data-ttu-id="dd14e-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd14e-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dd14e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd14e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd14e-138"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd14e-138"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd14e-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dd14e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd14e-140"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd14e-140"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd14e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dd14e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd14e-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd14e-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd14e-143">IID</span><span class="sxs-lookup"><span data-stu-id="dd14e-143">IID</span></span><br/>                      | <span data-ttu-id="dd14e-144">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dd14e-144">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="dd14e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd14e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd14e-146">**AttachByReader**</span><span class="sxs-lookup"><span data-stu-id="dd14e-146">**AttachByReader**</span></span>](iscard-attachbyreader.md)
</dt> <dt>

[<span data-ttu-id="dd14e-147">**Detach**</span><span class="sxs-lookup"><span data-stu-id="dd14e-147">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="dd14e-148">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="dd14e-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="dd14e-149">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="dd14e-149">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="dd14e-150">**Anexar novamente**</span><span class="sxs-lookup"><span data-stu-id="dd14e-150">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
