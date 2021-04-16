---
description: Recupera o byte de status de APDUs SW1 de resposta.
ms.assetid: 5f74d0c9-cf82-4694-bca6-a2655e717a1f
title: 'Método ISCardCmd:: get_ReplyStatusSW1 (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyStatusSW1
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92bcf490a3cb1fc533bcf9a1046642d3c3e55b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501755"
---
# <a name="iscardcmdget_replystatussw1-method"></a><span data-ttu-id="adf34-103">Método ISCardCmd:: get \_ ReplyStatusSW1</span><span class="sxs-lookup"><span data-stu-id="adf34-103">ISCardCmd::get\_ReplyStatusSW1 method</span></span>

<span data-ttu-id="adf34-104">\[O método **Get \_ ReplyStatusSW1** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="adf34-104">\[The **get\_ReplyStatusSW1** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="adf34-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="adf34-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="adf34-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="adf34-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="adf34-107">O método **Get \_ ReplyStatusSW1** recupera o byte de status de APDUs SW1 de [*resposta*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="adf34-107">The **get\_ReplyStatusSW1** method retrieves the [*reply APDUs*](../secgloss/r-gly.md) SW1 status byte.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf34-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adf34-108">Syntax</span></span>


```C++
HRESULT get_ReplyStatusSW1(
  [out] LPBYTE pbySW1
);
```



## <a name="parameters"></a><span data-ttu-id="adf34-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adf34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf34-110">*pbySW1* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="adf34-110">*pbySW1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adf34-111">Ponteiro para o byte que contém o valor do byte de SW1 no retorno.</span><span class="sxs-lookup"><span data-stu-id="adf34-111">Pointer to the byte that contains the value of the SW1 byte on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adf34-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adf34-112">Return value</span></span>

<span data-ttu-id="adf34-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="adf34-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="adf34-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="adf34-114">Return code</span></span>                                                                                   | <span data-ttu-id="adf34-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="adf34-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="adf34-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="adf34-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="adf34-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="adf34-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="adf34-119">O parâmetro *pbySW1* não é válido.</span><span class="sxs-lookup"><span data-stu-id="adf34-119">The *pbySW1* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="adf34-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="adf34-121">Um ponteiro inadequado foi passado em *pbySW1*.</span><span class="sxs-lookup"><span data-stu-id="adf34-121">A bad pointer was passed in *pbySW1*.</span></span><br/> |
| <dl> <span data-ttu-id="adf34-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="adf34-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="adf34-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="adf34-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="adf34-124">Remarks</span></span>

<span data-ttu-id="adf34-125">O byte de status de SW1 [*do APDU de resposta*](../secgloss/r-gly.md) é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="adf34-125">The [*reply APDU's*](../secgloss/r-gly.md) SW1 status byte is read-only.</span></span>

<span data-ttu-id="adf34-126">Para recuperar o byte de status do SW2 do APDU de resposta, chame [**Get \_ ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span><span class="sxs-lookup"><span data-stu-id="adf34-126">To retrieve the reply APDU's SW2 status byte, call [**get\_ReplyStatusSW2**](iscardcmd-get-replystatussw2.md).</span></span>

<span data-ttu-id="adf34-127">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="adf34-127">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="adf34-128">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="adf34-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="adf34-129">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="adf34-129">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="adf34-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="adf34-130">Examples</span></span>

<span data-ttu-id="adf34-131">O exemplo a seguir mostra como recuperar o byte de status de SW1 da [*resposta APDU*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="adf34-131">The following example shows how to retrieve the SW1 status byte of the [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="adf34-132">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="adf34-132">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE     bySW1;
HRESULT  hr;

// Retrieve the reply status SW1 byte.
hr = pISCardCmd->get_ReplyStatusSW1(&bySW1);
if (FAILED(hr))
{
  printf("Failed get_ReplyStatusSW1\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="adf34-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf34-133">Requirements</span></span>



| <span data-ttu-id="adf34-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf34-134">Requirement</span></span> | <span data-ttu-id="adf34-135">Valor</span><span class="sxs-lookup"><span data-stu-id="adf34-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adf34-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf34-136">Minimum supported client</span></span><br/> | <span data-ttu-id="adf34-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="adf34-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="adf34-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adf34-138">Minimum supported server</span></span><br/> | <span data-ttu-id="adf34-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="adf34-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adf34-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="adf34-140">End of client support</span></span><br/>    | <span data-ttu-id="adf34-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="adf34-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="adf34-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="adf34-142">End of server support</span></span><br/>    | <span data-ttu-id="adf34-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="adf34-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="adf34-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="adf34-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf34-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="adf34-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="adf34-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="adf34-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="adf34-148">DLL</span><span class="sxs-lookup"><span data-stu-id="adf34-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adf34-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adf34-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="adf34-150">IID</span><span class="sxs-lookup"><span data-stu-id="adf34-150">IID</span></span><br/>                      | <span data-ttu-id="adf34-151">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="adf34-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="adf34-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="adf34-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf34-153">**obter \_ ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="adf34-153">**get\_ReplyStatusSW2**</span></span>](iscardcmd-get-replystatussw2.md)
</dt> <dt>

[<span data-ttu-id="adf34-154">**obter \_ ReplyStatus**</span><span class="sxs-lookup"><span data-stu-id="adf34-154">**get\_ReplyStatus**</span></span>](iscardcmd-get-replystatus.md)
</dt> <dt>

[<span data-ttu-id="adf34-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="adf34-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
