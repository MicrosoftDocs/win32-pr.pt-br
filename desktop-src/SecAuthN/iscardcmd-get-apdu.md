---
description: Recupera a APDU (unidade de dados do protocolo de aplicativo bruto).
ms.assetid: d8b326db-de54-4ef8-becb-fd905414c45c
title: 'Método ISCardCmd:: get_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb943d7ade48f6684cdc10cb4b1ad7e48f87e65c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010510"
---
# <a name="iscardcmdget_apdu-method"></a><span data-ttu-id="b1e81-103">Método ISCardCmd:: get \_ APDU</span><span class="sxs-lookup"><span data-stu-id="b1e81-103">ISCardCmd::get\_Apdu method</span></span>

<span data-ttu-id="b1e81-104">\[O método **Get \_ APDU** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b1e81-104">\[The **get\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b1e81-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b1e81-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b1e81-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b1e81-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b1e81-107">O método **Get \_ APDU** recupera a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) bruto).</span><span class="sxs-lookup"><span data-stu-id="b1e81-107">The **get\_Apdu** method retrieves the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e81-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1e81-108">Syntax</span></span>


```C++
HRESULT get_Apdu(
  [out] LPBYTEBUFFER *ppApdu
);
```



## <a name="parameters"></a><span data-ttu-id="b1e81-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e81-110">*ppApdu* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b1e81-110">*ppApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e81-111">Ponteiro para o buffer de bytes mapeado por meio de um objeto **IStream** que contém a mensagem APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="b1e81-111">Pointer to the byte buffer mapped through an **IStream** object that contains the APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e81-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1e81-112">Return value</span></span>

<span data-ttu-id="b1e81-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="b1e81-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="b1e81-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1e81-114">Return code</span></span>                                                                                   | <span data-ttu-id="b1e81-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1e81-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b1e81-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b1e81-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b1e81-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="b1e81-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b1e81-119">O parâmetro *ppApdu* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b1e81-119">The *ppApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="b1e81-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b1e81-121">Um ponteiro inadequado foi passado em *ppApdu*.</span><span class="sxs-lookup"><span data-stu-id="b1e81-121">A bad pointer was passed in *ppApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="b1e81-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b1e81-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="b1e81-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="b1e81-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1e81-124">Remarks</span></span>

<span data-ttu-id="b1e81-125">Para copiar o APDU de um objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) para o APDU encapsulado neste objeto de interface, chame [**Put \_ APDU**](iscardcmd-put-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="b1e81-125">To copy the APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object, call [**put\_Apdu**](iscardcmd-put-apdu.md).</span></span>

<span data-ttu-id="b1e81-126">Para determinar o comprimento do APDU, chame [**Get \_ ApduLength**](iscardcmd-get-apdulength.md).</span><span class="sxs-lookup"><span data-stu-id="b1e81-126">To determine the length of the APDU, call [**get\_ApduLength**](iscardcmd-get-apdulength.md).</span></span>

<span data-ttu-id="b1e81-127">Para obter uma lista de todos os métodos fornecidos pela interface [**ISCardCmd**](iscardcmd.md) , consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="b1e81-127">For a list of all the methods provided by the [**ISCardCmd**](iscardcmd.md) interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="b1e81-128">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b1e81-128">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b1e81-129">Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b1e81-129">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b1e81-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b1e81-130">Examples</span></span>

<span data-ttu-id="b1e81-131">O exemplo a seguir mostra como recuperar a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) bruto).</span><span class="sxs-lookup"><span data-stu-id="b1e81-131">The following example shows how to retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="b1e81-132">O exemplo supõe que pISCardCmd é um ponteiro válido para a interface [**ISCardCmd**](iscardcmd.md) e que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b1e81-132">The example assumes that pISCardCmd is a valid pointer to the [**ISCardCmd**](iscardcmd.md) interface, and that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

hr = pISCardCmd->get_Apdu(&pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed get_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="b1e81-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e81-133">Requirements</span></span>



| <span data-ttu-id="b1e81-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e81-134">Requirement</span></span> | <span data-ttu-id="b1e81-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b1e81-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e81-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e81-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e81-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1e81-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b1e81-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1e81-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e81-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1e81-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1e81-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b1e81-140">End of client support</span></span><br/>    | <span data-ttu-id="b1e81-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b1e81-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="b1e81-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b1e81-142">End of server support</span></span><br/>    | <span data-ttu-id="b1e81-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1e81-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="b1e81-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1e81-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1e81-145"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-145"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1e81-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b1e81-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1e81-147"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-147"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1e81-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b1e81-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1e81-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e81-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1e81-150">IID</span><span class="sxs-lookup"><span data-stu-id="b1e81-150">IID</span></span><br/>                      | <span data-ttu-id="b1e81-151">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="b1e81-151">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b1e81-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1e81-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e81-153">**obter \_ ApduLength**</span><span class="sxs-lookup"><span data-stu-id="b1e81-153">**get\_ApduLength**</span></span>](iscardcmd-get-apdulength.md)
</dt> <dt>

[<span data-ttu-id="b1e81-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="b1e81-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="b1e81-155">**colocar \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="b1e81-155">**put\_Apdu**</span></span>](iscardcmd-put-apdu.md)
</dt> </dl>

 

 
