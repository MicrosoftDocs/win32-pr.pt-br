---
description: Recupera o estado atual do cartão inteligente.
ms.assetid: 0e6e4a8f-ecad-4a82-8804-aaf58f13f7ca
title: 'Método iscard:: get_Status (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Status
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0daa47653779b3aa4b5e7cb65c0c56410b19ab9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172000"
---
# <a name="iscardget_status-method"></a><span data-ttu-id="ba593-103">Método iscard:: obter \_ status</span><span class="sxs-lookup"><span data-stu-id="ba593-103">ISCard::get\_Status method</span></span>

<span data-ttu-id="ba593-104">\[O método **Get \_ status** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ba593-104">\[The **get\_Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ba593-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ba593-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ba593-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ba593-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ba593-107">O método **Get \_ status** recupera o [*estado*](../secgloss/s-gly.md) atual do [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ba593-107">The **get\_Status** method retrieves the current [*state*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba593-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba593-108">Syntax</span></span>


```C++
HRESULT get_Status(
  [out] SCARD_STATES *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ba593-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba593-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba593-110">*pStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ba593-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba593-111">Ponteiro para a variável de estado.</span><span class="sxs-lookup"><span data-stu-id="ba593-111">Pointer to the state variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba593-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba593-112">Return value</span></span>

<span data-ttu-id="ba593-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="ba593-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ba593-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba593-114">Return code</span></span>                                                                                  | <span data-ttu-id="ba593-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba593-115">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="ba593-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ba593-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ba593-117">Operation completed successfully.</span></span><br/>      |
| <dl> <span data-ttu-id="ba593-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ba593-119">O parâmetro *pStatus* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba593-119">The *pStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ba593-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ba593-121">Um ponteiro inadequado foi passado em *pStatus*.</span><span class="sxs-lookup"><span data-stu-id="ba593-121">A bad pointer was passed in *pStatus*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba593-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba593-122">Remarks</span></span>

<span data-ttu-id="ba593-123">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ba593-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ba593-124">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ba593-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ba593-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba593-125">Examples</span></span>

<span data-ttu-id="ba593-126">O exemplo a seguir mostra a recuperação do estado atual do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="ba593-126">The following example shows retrieving the current state of the smart card.</span></span>


```C++
SCARD_STATES    scState;
HRESULT         hr;

// Determine the current state of the smart card.
hr = pISCard->get_Status(&scState);
if (FAILED(hr))
{
   printf("Failed get_Status\n");
   exit(1);  // Or other error handling action.
}
// Use the retrieved value. (This example merely displays it.)
switch (scState)
{
    case ABSENT:
        printf("Absent state\n");
        break;
    case PRESENT:
        printf("Present state\n");
        break;
    case SWALLOWED:
        printf("Swallowed state\n");
        break;
    case POWERED:
        printf("Powered state\n");
        break;
    case NEGOTIABLEMODE:
        printf("Negotiable mode state\n");
        break;
    case SPECIFICMODE:
        printf("Specific mode state\n");
        break;
    default:
        printf("Unexpected state\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="ba593-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba593-127">Requirements</span></span>



| <span data-ttu-id="ba593-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba593-128">Requirement</span></span> | <span data-ttu-id="ba593-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ba593-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba593-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba593-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba593-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ba593-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ba593-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba593-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba593-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ba593-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba593-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ba593-134">End of client support</span></span><br/>    | <span data-ttu-id="ba593-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba593-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ba593-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ba593-136">End of server support</span></span><br/>    | <span data-ttu-id="ba593-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ba593-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ba593-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba593-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba593-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba593-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ba593-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba593-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ba593-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ba593-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba593-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba593-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ba593-144">IID</span><span class="sxs-lookup"><span data-stu-id="ba593-144">IID</span></span><br/>                      | <span data-ttu-id="ba593-145">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ba593-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ba593-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba593-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba593-147">**obter \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="ba593-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="ba593-148">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="ba593-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="ba593-149">**obter \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="ba593-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="ba593-150">**obter \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="ba593-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="ba593-151">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="ba593-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
