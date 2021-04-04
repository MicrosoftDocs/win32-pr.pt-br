---
description: O método LockSCard declara o acesso exclusivo ao cartão inteligente.
ms.assetid: 70af7c5a-ebe7-48ee-8a76-dfea7f73f45e
title: 'Método iscard:: LockSCard (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.LockSCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d5b834afec339aa4c3a4eee42f9817409fabb917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171251"
---
# <a name="iscardlockscard-method"></a><span data-ttu-id="25556-103">Método iscard:: LockSCard</span><span class="sxs-lookup"><span data-stu-id="25556-103">ISCard::LockSCard method</span></span>

<span data-ttu-id="25556-104">\[O método **LockSCard** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="25556-104">\[The **LockSCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="25556-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="25556-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="25556-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="25556-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="25556-107">O método **LockSCard** declara o acesso exclusivo ao [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="25556-107">The **LockSCard** method claims exclusive access to the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="25556-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25556-108">Syntax</span></span>


```C++
HRESULT LockSCard();
```



## <a name="parameters"></a><span data-ttu-id="25556-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25556-109">Parameters</span></span>

<span data-ttu-id="25556-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="25556-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25556-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25556-111">Return value</span></span>

<span data-ttu-id="25556-112">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="25556-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="25556-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="25556-113">Return code</span></span>                                                                          | <span data-ttu-id="25556-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="25556-114">Description</span></span>                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25556-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25556-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="25556-116">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="25556-116">Operation completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25556-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="25556-117">Remarks</span></span>

<span data-ttu-id="25556-118">Além do código de erro COM listado acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="25556-118">In addition to the COM error code listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="25556-119">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="25556-119">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="25556-120">Para desbloquear o cartão inteligente, chame o método [**iscard:: UnlockSCard**](iscard-unlockscard.md) .</span><span class="sxs-lookup"><span data-stu-id="25556-120">To unlock the smart card, call the [**ISCard::UnlockSCard**](iscard-unlockscard.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="25556-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25556-121">Examples</span></span>

<span data-ttu-id="25556-122">O exemplo a seguir mostra a aquisição de acesso exclusivo ao cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="25556-122">The following example shows acquiring exclusive access to the smart card.</span></span>


```C++
HRESULT    hr;

// Lock the smart card.
hr = pISCard->LockSCard();
if (FAILED(hr))
{
    printf("Failed LockSCard\n");
    // Take error handling action as needed.
}
// Use smart card; unlock the smart card when done.
```



## <a name="requirements"></a><span data-ttu-id="25556-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25556-123">Requirements</span></span>



| <span data-ttu-id="25556-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="25556-124">Requirement</span></span> | <span data-ttu-id="25556-125">Valor</span><span class="sxs-lookup"><span data-stu-id="25556-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25556-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25556-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25556-127">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25556-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25556-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25556-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25556-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25556-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25556-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="25556-130">End of client support</span></span><br/>    | <span data-ttu-id="25556-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="25556-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="25556-132">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="25556-132">End of server support</span></span><br/>    | <span data-ttu-id="25556-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25556-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="25556-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25556-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="25556-135"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="25556-135"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="25556-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="25556-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="25556-137"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25556-137"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25556-138">DLL</span><span class="sxs-lookup"><span data-stu-id="25556-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25556-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25556-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="25556-140">IID</span><span class="sxs-lookup"><span data-stu-id="25556-140">IID</span></span><br/>                      | <span data-ttu-id="25556-141">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="25556-141">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="25556-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="25556-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25556-143">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="25556-143">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="25556-144">**UnlockSCard**</span><span class="sxs-lookup"><span data-stu-id="25556-144">**UnlockSCard**</span></span>](iscard-unlockscard.md)
</dt> </dl>

 

 
