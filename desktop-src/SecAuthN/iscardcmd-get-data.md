---
description: Recupera o campo de dados da APDU (unidade de dados do protocolo de aplicativo), colocando-o em um objeto de buffer de bytes.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Método ISCardCmd:: get_Data (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506250"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="c63bc-103">Método ISCardCmd:: get \_ Data</span><span class="sxs-lookup"><span data-stu-id="c63bc-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="c63bc-104">\[O método **Get \_ Data** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c63bc-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c63bc-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c63bc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c63bc-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c63bc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c63bc-107">O método **Get \_ Data** recupera o campo de dados da APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ), colocando-o em um objeto de buffer de bytes.</span><span class="sxs-lookup"><span data-stu-id="c63bc-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63bc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c63bc-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="c63bc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c63bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c63bc-110">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c63bc-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c63bc-111">Ponteiro para o **IStream**(objeto de buffer de bytes) que contém o campo de dados APDU no retorno.</span><span class="sxs-lookup"><span data-stu-id="c63bc-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c63bc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c63bc-112">Return value</span></span>

<span data-ttu-id="c63bc-113">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="c63bc-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c63bc-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c63bc-114">Return code</span></span>                                                                                   | <span data-ttu-id="c63bc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c63bc-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c63bc-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c63bc-117">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="c63bc-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="c63bc-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c63bc-119">O parâmetro *ppData* não é válido.</span><span class="sxs-lookup"><span data-stu-id="c63bc-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c63bc-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c63bc-121">Um ponteiro inadequado foi passado em *ppData*.</span><span class="sxs-lookup"><span data-stu-id="c63bc-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="c63bc-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c63bc-123">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="c63bc-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="c63bc-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c63bc-124">Remarks</span></span>

<span data-ttu-id="c63bc-125">Para definir o campo de dados do APDU, chame [**Put \_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="c63bc-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="c63bc-126">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c63bc-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c63bc-127">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c63bc-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c63bc-128">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c63bc-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c63bc-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c63bc-129">Examples</span></span>

<span data-ttu-id="c63bc-130">O exemplo a seguir mostra como recuperar o campo de dados da [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="c63bc-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="c63bc-131">O exemplo supõe que pIByteData é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) e que pISCardCmd é um ponteiro válido para uma instância da interface [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c63bc-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c63bc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c63bc-132">Requirements</span></span>



| <span data-ttu-id="c63bc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c63bc-133">Requirement</span></span> | <span data-ttu-id="c63bc-134">Valor</span><span class="sxs-lookup"><span data-stu-id="c63bc-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c63bc-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c63bc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c63bc-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c63bc-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c63bc-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c63bc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c63bc-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c63bc-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c63bc-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c63bc-139">End of client support</span></span><br/>    | <span data-ttu-id="c63bc-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c63bc-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c63bc-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c63bc-141">End of server support</span></span><br/>    | <span data-ttu-id="c63bc-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c63bc-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c63bc-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c63bc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c63bc-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c63bc-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c63bc-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="c63bc-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c63bc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c63bc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c63bc-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63bc-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c63bc-149">IID</span><span class="sxs-lookup"><span data-stu-id="c63bc-149">IID</span></span><br/>                      | <span data-ttu-id="c63bc-150">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c63bc-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c63bc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c63bc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63bc-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="c63bc-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="c63bc-153">**colocar \_ dados**</span><span class="sxs-lookup"><span data-stu-id="c63bc-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
