---
description: Copia a APDU (unidade de dados do protocolo de aplicativo) do objeto IByteBuffer (IStream) para o APDU encapsulado neste objeto de interface.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'ISCardCmd: método de ut_Apdu de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920928"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="ead9b-103">ISCardCmd: método UT \_ Apdu:p</span><span class="sxs-lookup"><span data-stu-id="ead9b-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="ead9b-104">\[O método **Put \_ APDU** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="ead9b-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ead9b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ead9b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ead9b-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ead9b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ead9b-107">O **método Put \_ APDU** copia a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) do objeto [**IBYTEBUFFER**](ibytebuffer.md) (**IStream**) para o APDU encapsulado neste objeto de interface.</span><span class="sxs-lookup"><span data-stu-id="ead9b-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead9b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ead9b-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="ead9b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ead9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead9b-110">*pApdu* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ead9b-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead9b-111">Ponteiro para o APDU ISO 7816-4 a ser copiado no.</span><span class="sxs-lookup"><span data-stu-id="ead9b-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead9b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-112">Return value</span></span>

<span data-ttu-id="ead9b-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="ead9b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ead9b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ead9b-114">Return code</span></span>                                                                                   | <span data-ttu-id="ead9b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ead9b-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ead9b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ead9b-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ead9b-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="ead9b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ead9b-119">O parâmetro *pApdu* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ead9b-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ead9b-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ead9b-121">Um ponteiro inadequado foi passado em *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="ead9b-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="ead9b-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ead9b-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="ead9b-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="ead9b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ead9b-124">Remarks</span></span>

<span data-ttu-id="ead9b-125">Para recuperar o APDU bruto do buffer de bytes mapeado por meio de um **IStream** que contém a mensagem APDU, chame [**Get \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="ead9b-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="ead9b-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ead9b-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ead9b-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ead9b-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ead9b-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ead9b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ead9b-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ead9b-129">Examples</span></span>

<span data-ttu-id="ead9b-130">O exemplo a seguir mostra como copiar um APDU de um objeto [**IByteBuffer**](ibytebuffer.md) (**IStream**) para o APDU encapsulado em um objeto de interface.</span><span class="sxs-lookup"><span data-stu-id="ead9b-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="ead9b-131">O exemplo supõe que pIByteApdu é um ponteiro válido para uma instância de **IByteBuffer** e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="ead9b-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ead9b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead9b-132">Requirements</span></span>



| <span data-ttu-id="ead9b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead9b-133">Requirement</span></span> | <span data-ttu-id="ead9b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ead9b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ead9b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ead9b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ead9b-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ead9b-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ead9b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ead9b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ead9b-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ead9b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ead9b-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ead9b-139">End of client support</span></span><br/>    | <span data-ttu-id="ead9b-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ead9b-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ead9b-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ead9b-141">End of server support</span></span><br/>    | <span data-ttu-id="ead9b-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ead9b-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ead9b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ead9b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead9b-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ead9b-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ead9b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ead9b-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ead9b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ead9b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead9b-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead9b-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ead9b-149">IID</span><span class="sxs-lookup"><span data-stu-id="ead9b-149">IID</span></span><br/>                      | <span data-ttu-id="ead9b-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ead9b-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ead9b-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="ead9b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead9b-152">**obter \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="ead9b-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="ead9b-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ead9b-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
