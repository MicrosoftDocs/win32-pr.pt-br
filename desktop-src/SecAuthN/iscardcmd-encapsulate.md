---
description: O método encapsulate encapsula a APDU (unidade de dados do protocolo de aplicativo) de comando fornecida em outro APDU de comando para transmissão para um cartão inteligente.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Método ISCardCmd:: encapsulate (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748552"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="aa990-103">Método ISCardCmd:: encapsulate</span><span class="sxs-lookup"><span data-stu-id="aa990-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="aa990-104">\[O método **encapsulate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="aa990-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="aa990-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aa990-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aa990-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="aa990-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="aa990-107">O método **encapsulate** encapsula a APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) de comando fornecida em outro APDU de comando para transmissão para um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="aa990-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa990-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa990-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="aa990-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa990-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa990-110">*pApdu* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa990-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa990-111">Ponteiro para o APDU a ser encapsulado.</span><span class="sxs-lookup"><span data-stu-id="aa990-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="aa990-112">*ApduType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa990-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa990-113">Caso ISO 7816-4 para transmissões [*T = 0*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="aa990-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="aa990-114">**\_Caso ISO \_ 1**</span><span class="sxs-lookup"><span data-stu-id="aa990-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="aa990-115">**\_Caso ISO \_ 2**</span><span class="sxs-lookup"><span data-stu-id="aa990-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="aa990-116">**\_Caso ISO \_ 3**</span><span class="sxs-lookup"><span data-stu-id="aa990-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="aa990-117">**\_Caso ISO \_ 4**</span><span class="sxs-lookup"><span data-stu-id="aa990-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa990-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa990-118">Return value</span></span>

<span data-ttu-id="aa990-119">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="aa990-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="aa990-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aa990-120">Return code</span></span>                                                                                   | <span data-ttu-id="aa990-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa990-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="aa990-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aa990-123">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="aa990-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="aa990-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="aa990-125">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="aa990-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="aa990-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aa990-127">Um ponteiro inadequado foi passado em *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="aa990-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="aa990-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aa990-129">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="aa990-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="aa990-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa990-130">Remarks</span></span>

<span data-ttu-id="aa990-131">Para criar um comando APDU, chame [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="aa990-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="aa990-132">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="aa990-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="aa990-133">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="aa990-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="aa990-134">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="aa990-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aa990-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aa990-135">Examples</span></span>

<span data-ttu-id="aa990-136">O exemplo a seguir mostra como encapsular um comando APDU.</span><span class="sxs-lookup"><span data-stu-id="aa990-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="aa990-137">O exemplo supõe que pIByteApdu é um ponteiro válido para uma instância da interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="aa990-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="aa990-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa990-138">Requirements</span></span>



| <span data-ttu-id="aa990-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa990-139">Requirement</span></span> | <span data-ttu-id="aa990-140">Valor</span><span class="sxs-lookup"><span data-stu-id="aa990-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa990-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa990-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aa990-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aa990-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="aa990-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa990-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aa990-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa990-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa990-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="aa990-145">End of client support</span></span><br/>    | <span data-ttu-id="aa990-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa990-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="aa990-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="aa990-147">End of server support</span></span><br/>    | <span data-ttu-id="aa990-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aa990-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="aa990-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa990-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa990-150"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa990-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa990-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa990-152"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa990-153">DLL</span><span class="sxs-lookup"><span data-stu-id="aa990-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa990-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa990-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa990-155">IID</span><span class="sxs-lookup"><span data-stu-id="aa990-155">IID</span></span><br/>                      | <span data-ttu-id="aa990-156">IID \_ ISCardCmd é definido como D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="aa990-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="aa990-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa990-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa990-158">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="aa990-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="aa990-159">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="aa990-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
