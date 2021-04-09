---
description: Recupera o endereço do nó (NAD) usado pelo cartão inteligente na mensagem de resposta.
ms.assetid: bf4f281c-d378-4abd-8f2e-e23c2f4e87a4
title: 'Método ISCardCmd:: get_ReplyNad (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ReplyNad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2088aa208a97511fd53eecec5a8cdc473b612bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090464"
---
# <a name="iscardcmdget_replynad-method"></a><span data-ttu-id="db605-103">Método ISCardCmd:: get \_ ReplyNad</span><span class="sxs-lookup"><span data-stu-id="db605-103">ISCardCmd::get\_ReplyNad method</span></span>

<span data-ttu-id="db605-104">\[O método **Get \_ ReplyNad** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="db605-104">\[The **get\_ReplyNad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="db605-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="db605-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db605-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="db605-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="db605-107">O método **Get \_ ReplyNad** recupera o endereço de nó (NAD) usado pelo [*cartão inteligente*](../secgloss/s-gly.md) na mensagem de resposta.</span><span class="sxs-lookup"><span data-stu-id="db605-107">The **get\_ReplyNad** method retrieves the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span>

## <a name="syntax"></a><span data-ttu-id="db605-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db605-108">Syntax</span></span>


```C++
HRESULT get_ReplyNad(
  [out] BYTE *pbNad
);
```



## <a name="parameters"></a><span data-ttu-id="db605-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db605-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db605-110">*pbNad* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="db605-110">*pbNad* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db605-111">Ponteiro para o byte que contém o NAD usado pela mensagem de resposta, no retorno.</span><span class="sxs-lookup"><span data-stu-id="db605-111">Pointer to the byte that contains the Nad used by the reply message, on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db605-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db605-112">Return value</span></span>

<span data-ttu-id="db605-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="db605-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="db605-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="db605-114">Return code</span></span>                                                                                    | <span data-ttu-id="db605-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="db605-115">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="db605-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db605-116"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="db605-117">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="db605-117">Operation was completed successfully.</span></span><br/>                   |
| <dl> <span data-ttu-id="db605-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="db605-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="db605-119">O parâmetro *pbNad* não é válido.</span><span class="sxs-lookup"><span data-stu-id="db605-119">The *pbNad* parameter is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="db605-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="db605-120"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl> | <span data-ttu-id="db605-121">Chamadas internas não puderam recuperar informações da NAD.</span><span class="sxs-lookup"><span data-stu-id="db605-121">Internal calls were unable to retrieve Nad information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db605-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="db605-122">Remarks</span></span>

<span data-ttu-id="db605-123">Além dos códigos de erro COM listados acima, esse método pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="db605-123">In addition to the COM error codes listed above, this method may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="db605-124">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="db605-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="db605-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="db605-125">Examples</span></span>

<span data-ttu-id="db605-126">O exemplo a seguir mostra como recuperar o endereço do nó (NAD) usado pelo [*cartão inteligente*](../secgloss/s-gly.md) na mensagem de resposta.</span><span class="sxs-lookup"><span data-stu-id="db605-126">The following example shows how to retrieve the node address (Nad) used by the [*smart card*](../secgloss/s-gly.md) in the reply message.</span></span> <span data-ttu-id="db605-127">O exemplo supõe que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="db605-127">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
BYTE    byNad;
HRESULT hr;

// Get reply Nad.
hr = pISCardCmd->get_ReplyNad(&byNad);
if (FAILED(hr))
{
  printf("Failed get_ReplyNad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="db605-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db605-128">Requirements</span></span>



| <span data-ttu-id="db605-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="db605-129">Requirement</span></span> | <span data-ttu-id="db605-130">Valor</span><span class="sxs-lookup"><span data-stu-id="db605-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db605-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db605-131">Minimum supported client</span></span><br/> | <span data-ttu-id="db605-132">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="db605-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="db605-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db605-133">Minimum supported server</span></span><br/> | <span data-ttu-id="db605-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db605-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db605-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="db605-135">End of client support</span></span><br/>    | <span data-ttu-id="db605-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="db605-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="db605-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="db605-137">End of server support</span></span><br/>    | <span data-ttu-id="db605-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db605-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="db605-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db605-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="db605-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="db605-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="db605-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="db605-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="db605-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db605-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db605-143">DLL</span><span class="sxs-lookup"><span data-stu-id="db605-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db605-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db605-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db605-145">IID</span><span class="sxs-lookup"><span data-stu-id="db605-145">IID</span></span><br/>                      | <span data-ttu-id="db605-146">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="db605-146">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="db605-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="db605-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db605-148">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="db605-148">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
