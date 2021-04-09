---
description: Recupera o APDU de resposta, colocando-o em um buffer de bytes específico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Método ISCardCmd:: get_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011804"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="01229-103">Método ISCardCmd:: get \_ ApduReply</span><span class="sxs-lookup"><span data-stu-id="01229-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="01229-104">\[O método **Get \_ ApduReply** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="01229-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="01229-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="01229-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="01229-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="01229-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="01229-107">O método **Get \_ ApduReply** recupera o [*APDU de resposta*](../secgloss/r-gly.md), colocando-o em um buffer de bytes específico.</span><span class="sxs-lookup"><span data-stu-id="01229-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="01229-108">A resposta poderá ser **nula** se nenhuma [*transação*](../secgloss/t-gly.md) tiver sido executada no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="01229-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="01229-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01229-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="01229-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01229-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01229-111">*ppReplyApdu* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01229-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01229-112">Ponteiro para o buffer de bytes (mapeado por meio de um objeto **IStream** ) que contém a mensagem de resposta APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="01229-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01229-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01229-113">Return value</span></span>

<span data-ttu-id="01229-114">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="01229-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="01229-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01229-115">Return code</span></span>                                                                                   | <span data-ttu-id="01229-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="01229-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="01229-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01229-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="01229-118">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="01229-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="01229-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="01229-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="01229-120">O parâmetro *ppReplyApdu* não é válido.</span><span class="sxs-lookup"><span data-stu-id="01229-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="01229-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="01229-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="01229-122">Um ponteiro inadequado foi passado em *ppReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="01229-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="01229-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="01229-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="01229-124">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="01229-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="01229-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="01229-125">Remarks</span></span>

<span data-ttu-id="01229-126">Para determinar o comprimento da resposta APDU, chame [**Get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="01229-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="01229-127">Para definir uma nova resposta APDU, chame [**Put \_ ApduReply**](iscardcmd-put-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="01229-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="01229-128">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="01229-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="01229-129">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="01229-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="01229-130">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="01229-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="01229-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01229-131">Examples</span></span>

<span data-ttu-id="01229-132">O exemplo a seguir mostra como recuperar dados de resposta.</span><span class="sxs-lookup"><span data-stu-id="01229-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="01229-133">O exemplo supõe que lLe é uma variável do tipo **Long** cujo valor foi definido por uma chamada anterior para o [**método ISCardCmd:: get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , que pIByteReply é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="01229-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="01229-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01229-134">Requirements</span></span>



| <span data-ttu-id="01229-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="01229-135">Requirement</span></span> | <span data-ttu-id="01229-136">Valor</span><span class="sxs-lookup"><span data-stu-id="01229-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01229-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01229-137">Minimum supported client</span></span><br/> | <span data-ttu-id="01229-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01229-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01229-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01229-139">Minimum supported server</span></span><br/> | <span data-ttu-id="01229-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01229-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01229-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="01229-141">End of client support</span></span><br/>    | <span data-ttu-id="01229-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01229-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="01229-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="01229-143">End of server support</span></span><br/>    | <span data-ttu-id="01229-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01229-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="01229-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01229-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="01229-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="01229-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="01229-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="01229-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="01229-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01229-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01229-149">DLL</span><span class="sxs-lookup"><span data-stu-id="01229-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01229-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01229-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01229-151">IID</span><span class="sxs-lookup"><span data-stu-id="01229-151">IID</span></span><br/>                      | <span data-ttu-id="01229-152">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="01229-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="01229-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="01229-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01229-154">**obter \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="01229-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="01229-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="01229-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="01229-156">**colocar \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="01229-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
