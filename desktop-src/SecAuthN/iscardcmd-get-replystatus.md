---
description: Recupera a palavra de status da mensagem do APDU de resposta.
ms.assetid: c8a4b713-4ae9-49f2-a623-6ee305123638
title: 'Método ISCardCmd:: get_ReplyStatus (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 021c5395dbca6275161a53cb7e8a0c2247ab9410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090463"
---
# <a name="iscardcmdget_replystatus-method"></a><span data-ttu-id="933fc-103">Método ISCardCmd:: get \_ ReplyStatus</span><span class="sxs-lookup"><span data-stu-id="933fc-103">ISCardCmd::get\_ReplyStatus method</span></span>

<span data-ttu-id="933fc-104">\[O método **Get \_ ReplyStatus** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="933fc-104">\[The **get\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="933fc-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="933fc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="933fc-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="933fc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="933fc-107">O método **Get \_ ReplyStatus** recupera a palavra de status [*da mensagem APDU de resposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="933fc-107">The **get\_ReplyStatus** method retrieves the [*reply APDU's*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="933fc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="933fc-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatus(
  [out] LPWORD pwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="933fc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="933fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933fc-110">*pwStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="933fc-110">*pwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="933fc-111">Ponteiro para a palavra que é o status no retorno.</span><span class="sxs-lookup"><span data-stu-id="933fc-111">Pointer to the word that is the status on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933fc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="933fc-112">Return value</span></span>

<span data-ttu-id="933fc-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="933fc-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="933fc-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="933fc-114">Return code</span></span>                                                                                   | <span data-ttu-id="933fc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="933fc-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="933fc-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="933fc-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="933fc-117">Operation completed successfully.</span></span><br/>       |
| <dl> <span data-ttu-id="933fc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="933fc-119">O parâmetro *pwStatus* não é válido.</span><span class="sxs-lookup"><span data-stu-id="933fc-119">The *pwStatus* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="933fc-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="933fc-121">Um ponteiro inadequado foi passado em *pwStatus*.</span><span class="sxs-lookup"><span data-stu-id="933fc-121">A bad pointer was passed in *pwStatus*.</span></span><br/> |
| <dl> <span data-ttu-id="933fc-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="933fc-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="933fc-123">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="933fc-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="933fc-124">Remarks</span></span>

<span data-ttu-id="933fc-125">Para definir a palavra status da mensagem do Reply APDU, chame [**Put \_ ReplyStatus**](iscardcmd-put-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="933fc-125">To set the reply APDU's message status word, call [**put\_ReplyStatus**](iscardcmd-put-replystatus.md).</span></span>

<span data-ttu-id="933fc-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="933fc-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="933fc-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="933fc-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="933fc-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="933fc-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="933fc-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="933fc-129">Examples</span></span>

<span data-ttu-id="933fc-130">O exemplo a seguir mostra como recuperar a palavra de status da mensagem da [*resposta APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="933fc-130">The following example shows how to retrieve the message status word of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="933fc-131">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="933fc-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD    wReplyStatus;
HRESULT hr;

// Get reply status.
hr = pISCardCmd->get_ReplyStatus(&wReplyStatus);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatus\n");
  // Take other error handling action as needed.
}
else
{
  if (wReplyStatus != 0x9000)
  {
    printf("APDU failed - Error [0x%x]\n", wReplyStatus);
    // Take other error handling action as needed.
  }
}
```



## <a name="requirements"></a><span data-ttu-id="933fc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="933fc-132">Requirements</span></span>



| <span data-ttu-id="933fc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="933fc-133">Requirement</span></span> | <span data-ttu-id="933fc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="933fc-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="933fc-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="933fc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="933fc-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="933fc-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="933fc-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="933fc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="933fc-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="933fc-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="933fc-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="933fc-139">End of client support</span></span><br/>    | <span data-ttu-id="933fc-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="933fc-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="933fc-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="933fc-141">End of server support</span></span><br/>    | <span data-ttu-id="933fc-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="933fc-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="933fc-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="933fc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="933fc-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="933fc-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="933fc-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="933fc-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="933fc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="933fc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="933fc-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="933fc-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="933fc-149">IID</span><span class="sxs-lookup"><span data-stu-id="933fc-149">IID</span></span><br/>                      | <span data-ttu-id="933fc-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="933fc-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="933fc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="933fc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933fc-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="933fc-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="933fc-153">**colocar \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="933fc-153">**put\_ReplyStatus**</span></span>](iscardcmd-put-replystatus.md)
</dt> </dl>

 

 
