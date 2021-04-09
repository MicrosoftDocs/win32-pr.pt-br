---
description: Recupera o byte de status APDU do SW2 de resposta.
ms.assetid: 24ad0164-84fc-4a99-b9dd-0f7d789dff92
title: 'Método ISCardCmd:: get_ReplyStatusSW2 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW2
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7ff503758a50437b4b7ff974fe4455d4b92ce978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090462"
---
# <a name="iscardcmdget_replystatussw2-method"></a><span data-ttu-id="fb4ea-103">Método ISCardCmd:: get \_ ReplyStatusSW2</span><span class="sxs-lookup"><span data-stu-id="fb4ea-103">ISCardCmd::get\_ReplyStatusSW2 method</span></span>

<span data-ttu-id="fb4ea-104">\[O método **Get \_ ReplyStatusSW2** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-104">\[The **get\_ReplyStatusSW2** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb4ea-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb4ea-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="fb4ea-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fb4ea-107">O método **Get \_ ReplyStatusSW2** recupera o byte de status de [*resposta do APDU*](../secgloss/r-gly.md) SW2.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-107">The **get\_ReplyStatusSW2** method retrieves the [*reply APDU*](../secgloss/r-gly.md) SW2 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb4ea-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW2(
  [out] LPBYTE pbySW2
);
```



## <a name="parameters"></a><span data-ttu-id="fb4ea-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb4ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4ea-110">*pbySW2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fb4ea-110">*pbySW2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4ea-111">Ponteiro para o byte que contém o valor do byte SW2 no retorno.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-111">Pointer to the byte that contains the value of the SW2 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4ea-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb4ea-112">Return value</span></span>

<span data-ttu-id="fb4ea-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fb4ea-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fb4ea-114">Return code</span></span>                                                                                   | <span data-ttu-id="fb4ea-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb4ea-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fb4ea-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb4ea-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="fb4ea-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fb4ea-119">O *pbySW2* não é válido.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-119">The *pbySW2* is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="fb4ea-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fb4ea-121">Um ponteiro inadequado foi passado em *pbySW2*.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-121">A bad pointer was passed in *pbySW2*.</span></span><br/> |
| <dl> <span data-ttu-id="fb4ea-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb4ea-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="fb4ea-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb4ea-124">Remarks</span></span>

<span data-ttu-id="fb4ea-125">O byte de status do SW2 do APDU de resposta é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-125">The reply APDU's SW2 status byte is read-only.</span></span>

<span data-ttu-id="fb4ea-126">Para recuperar o byte de status de SW1 do APDU de resposta, chame [**Get \_ ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span><span class="sxs-lookup"><span data-stu-id="fb4ea-126">To retrieve the reply APDU's SW1 status byte, call [**get\_ReplyStatusSW1**](iscardcmd-get-replystatussw1.md).</span></span>

<span data-ttu-id="fb4ea-127">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="fb4ea-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="fb4ea-128">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="fb4ea-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fb4ea-129">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fb4ea-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fb4ea-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb4ea-130">Examples</span></span>

<span data-ttu-id="fb4ea-131">O exemplo a seguir mostra como recuperar o byte de status do SW2 do [*APDU de resposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fb4ea-131">The following example shows how to retrieve the SW2 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="fb4ea-132">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="fb4ea-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW2;
HRESULT  hr;

// Retrieve the reply status SW2 byte.
hr = pISCardCmd->get_ReplyStatusSW2(&bySW2);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW2\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="fb4ea-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb4ea-133">Requirements</span></span>



| <span data-ttu-id="fb4ea-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4ea-134">Requirement</span></span> | <span data-ttu-id="fb4ea-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fb4ea-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4ea-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4ea-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fb4ea-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb4ea-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb4ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4ea-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb4ea-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb4ea-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fb4ea-140">End of client support</span></span><br/>    | <span data-ttu-id="fb4ea-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb4ea-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fb4ea-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fb4ea-142">End of server support</span></span><br/>    | <span data-ttu-id="fb4ea-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb4ea-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fb4ea-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb4ea-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb4ea-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb4ea-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fb4ea-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb4ea-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb4ea-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fb4ea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb4ea-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4ea-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb4ea-150">IID</span><span class="sxs-lookup"><span data-stu-id="fb4ea-150">IID</span></span><br/>                      | <span data-ttu-id="fb4ea-151">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="fb4ea-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="fb4ea-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb4ea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4ea-153">**obter \_ ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="fb4ea-153">**get\_ReplyStatusSW1**</span></span>](iscardcmd-get-replystatussw1.md)
</dt> <dt>

[<span data-ttu-id="fb4ea-154">**obter \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="fb4ea-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="fb4ea-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="fb4ea-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
