---
description: Define uma nova palavra de status de mensagem APDU de resposta.
ms.assetid: 17b498eb-2268-451a-9f5c-c53cb7e42019
title: 'ISCardCmd: método de ut_ReplyStatus de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ReplyStatus
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 55e6de81cd7e2c98b527d0852ea31a25f8256c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089945"
---
# <a name="iscardcmdput_replystatus-method"></a><span data-ttu-id="97eaf-103">ISCardCmd: método UT \_ ReplyStatus:p</span><span class="sxs-lookup"><span data-stu-id="97eaf-103">ISCardCmd::put\_ReplyStatus method</span></span>

<span data-ttu-id="97eaf-104">\[O método **Put \_ ReplyStatus** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="97eaf-104">\[The **put\_ReplyStatus** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97eaf-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="97eaf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="97eaf-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="97eaf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="97eaf-107">O método **Put \_ ReplyStatus** define uma nova palavra de status de mensagem [*APDU de resposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="97eaf-107">The **put\_ReplyStatus** method sets a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span>

## <a name="syntax"></a><span data-ttu-id="97eaf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97eaf-108">Syntax</span></span>


```C++
HRESULT put_ReplyStatus(
  [in] WORD wStatus
);
```



## <a name="parameters"></a><span data-ttu-id="97eaf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97eaf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97eaf-110">*wStatus* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97eaf-110">*wStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97eaf-111">Palavra que é o status.</span><span class="sxs-lookup"><span data-stu-id="97eaf-111">Word that is the status.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97eaf-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97eaf-112">Return value</span></span>

<span data-ttu-id="97eaf-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="97eaf-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="97eaf-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="97eaf-114">Return code</span></span>                                                                                   | <span data-ttu-id="97eaf-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="97eaf-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="97eaf-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="97eaf-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="97eaf-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="97eaf-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="97eaf-119">O parâmetro *wStatus* não é válido.</span><span class="sxs-lookup"><span data-stu-id="97eaf-119">The *wStatus* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="97eaf-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="97eaf-121">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="97eaf-121">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="97eaf-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="97eaf-122">Remarks</span></span>

<span data-ttu-id="97eaf-123">Para obter a palavra de status da mensagem de resposta do APDU, chame [**Get \_ ReplyStatus**](iscardcmd-get-replystatus.md).</span><span class="sxs-lookup"><span data-stu-id="97eaf-123">To get the reply APDU's message status word, call [**get\_ReplyStatus**](iscardcmd-get-replystatus.md).</span></span>

<span data-ttu-id="97eaf-124">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="97eaf-124">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="97eaf-125">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="97eaf-125">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="97eaf-126">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="97eaf-126">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="97eaf-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97eaf-127">Examples</span></span>

<span data-ttu-id="97eaf-128">O exemplo a seguir mostra como definir uma nova palavra de status de mensagem [*APDU de resposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="97eaf-128">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md) message status word.</span></span> <span data-ttu-id="97eaf-129">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="97eaf-129">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
WORD     wNewStatus = 0x0000;
HRESULT  hr;

// Set reply status.
hr = pISCardCmd->put_ReplyStatus(wNewStatus);
if (FAILED(hr))
{
  printf("Failed put_ReplyStatus\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="97eaf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97eaf-130">Requirements</span></span>



| <span data-ttu-id="97eaf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="97eaf-131">Requirement</span></span> | <span data-ttu-id="97eaf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="97eaf-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97eaf-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97eaf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="97eaf-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97eaf-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97eaf-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97eaf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="97eaf-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97eaf-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97eaf-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="97eaf-137">End of client support</span></span><br/>    | <span data-ttu-id="97eaf-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="97eaf-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="97eaf-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="97eaf-139">End of server support</span></span><br/>    | <span data-ttu-id="97eaf-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="97eaf-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="97eaf-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97eaf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="97eaf-142"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-142"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="97eaf-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="97eaf-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="97eaf-144"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-144"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97eaf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="97eaf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97eaf-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97eaf-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="97eaf-147">IID</span><span class="sxs-lookup"><span data-stu-id="97eaf-147">IID</span></span><br/>                      | <span data-ttu-id="97eaf-148">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="97eaf-148">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="97eaf-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="97eaf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97eaf-150">**obter \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="97eaf-150">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="97eaf-151">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="97eaf-151">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
