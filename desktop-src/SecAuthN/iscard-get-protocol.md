---
description: Recupera o identificador do protocolo atualmente em uso no cartão inteligente.
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'Método iscard:: get_Protocol (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297259"
---
# <a name="iscardget_protocol-method"></a><span data-ttu-id="8adcc-103">Método de protocolo iscard:: get \_</span><span class="sxs-lookup"><span data-stu-id="8adcc-103">ISCard::get\_Protocol method</span></span>

<span data-ttu-id="8adcc-104">\[O método **Get \_ Protocol** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8adcc-104">\[The **get\_Protocol** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8adcc-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8adcc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8adcc-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8adcc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8adcc-107">O método **Get \_ Protocol** recupera o identificador do protocolo atualmente em uso no [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8adcc-107">The **get\_Protocol** method retrieves the identifier of the protocol currently in use on the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8adcc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8adcc-108">Syntax</span></span>


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="8adcc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8adcc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adcc-110">*pProtocol* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8adcc-110">*pProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8adcc-111">Ponteiro para o identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8adcc-111">Pointer to the protocol identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adcc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8adcc-112">Return value</span></span>

<span data-ttu-id="8adcc-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="8adcc-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8adcc-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8adcc-114">Return code</span></span>                                                                                  | <span data-ttu-id="8adcc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8adcc-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8adcc-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8adcc-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8adcc-117">Operation completed successfully.</span></span><br/>        |
| <dl> <span data-ttu-id="8adcc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8adcc-119">O parâmetro *pProtocol* não é válido.</span><span class="sxs-lookup"><span data-stu-id="8adcc-119">The *pProtocol* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="8adcc-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="8adcc-121">Um ponteiro inadequado foi passado em *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="8adcc-121">A bad pointer was passed in *pProtocol*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8adcc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8adcc-122">Remarks</span></span>

<span data-ttu-id="8adcc-123">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8adcc-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8adcc-124">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8adcc-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8adcc-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8adcc-125">Examples</span></span>

<span data-ttu-id="8adcc-126">O exemplo a seguir mostra a recuperação do identificador do protocolo atualmente em uso no cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="8adcc-126">The following example shows retrieving the identifier of the protocol currently in use on the smart card.</span></span>


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
}
```



## <a name="requirements"></a><span data-ttu-id="8adcc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8adcc-127">Requirements</span></span>



| <span data-ttu-id="8adcc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8adcc-128">Requirement</span></span> | <span data-ttu-id="8adcc-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8adcc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8adcc-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adcc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8adcc-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8adcc-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8adcc-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8adcc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8adcc-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8adcc-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8adcc-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8adcc-134">End of client support</span></span><br/>    | <span data-ttu-id="8adcc-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8adcc-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8adcc-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8adcc-136">End of server support</span></span><br/>    | <span data-ttu-id="8adcc-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8adcc-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8adcc-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8adcc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8adcc-139"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-139"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="8adcc-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8adcc-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="8adcc-141"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-141"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8adcc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8adcc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8adcc-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8adcc-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8adcc-144">IID</span><span class="sxs-lookup"><span data-stu-id="8adcc-144">IID</span></span><br/>                      | <span data-ttu-id="8adcc-145">\_O IID iscard é definido como 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8adcc-145">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8adcc-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8adcc-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8adcc-147">**obter \_ ATR**</span><span class="sxs-lookup"><span data-stu-id="8adcc-147">**get\_Atr**</span></span>](iscard-get-atr.md)
</dt> <dt>

[<span data-ttu-id="8adcc-148">**obter \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="8adcc-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="8adcc-149">**obter \_ contexto**</span><span class="sxs-lookup"><span data-stu-id="8adcc-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="8adcc-150">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="8adcc-150">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="8adcc-151">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="8adcc-151">**ISCard**</span></span>](iscard.md)
</dt> </dl>

 

 
