---
description: Constrói um comando APDU (unidade de dados do protocolo de aplicativo) que atualiza condicionalmente o status de segurança, verificando a identidade do computador quando o cartão inteligente não confia nele.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'Método ISCardISO7816:: ExternalAuthenticate (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370666"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="a65d7-103">Método ISCardISO7816:: ExternalAuthenticate</span><span class="sxs-lookup"><span data-stu-id="a65d7-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="a65d7-104">\[O método **ExternalAuthenticate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a65d7-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a65d7-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a65d7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a65d7-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a65d7-107">O método **ExternalAuthenticate** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que atualiza condicionalmente o status de segurança, verificando a identidade do computador quando o [*cartão inteligente*](../secgloss/s-gly.md) não confia nele.</span><span class="sxs-lookup"><span data-stu-id="a65d7-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="a65d7-108">O comando usa o resultado (Sim ou não) do cálculo pelo cartão (com base em um desafio emitido anteriormente pelo cartão, por exemplo, pelo \_ comando ins get \_ Challenge), uma chave (possivelmente segredo) armazenada no cartão e os dados de autenticação transmitidos pelo dispositivo de interface.</span><span class="sxs-lookup"><span data-stu-id="a65d7-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65d7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a65d7-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a65d7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a65d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65d7-111">*byAlgorithmRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65d7-112">A referência do algoritmo no cartão.</span><span class="sxs-lookup"><span data-stu-id="a65d7-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="a65d7-113">Se esse valor for zero, isso indica que nenhuma informação é fornecida.</span><span class="sxs-lookup"><span data-stu-id="a65d7-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="a65d7-114">A referência do algoritmo é conhecida antes de emitir o comando ou é fornecida no campo de dados.</span><span class="sxs-lookup"><span data-stu-id="a65d7-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="a65d7-115">*bySecretRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65d7-116">A referência do segredo.</span><span class="sxs-lookup"><span data-stu-id="a65d7-116">The reference of the secret.</span></span>



| <span data-ttu-id="a65d7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a65d7-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="a65d7-118">Significado</span><span class="sxs-lookup"><span data-stu-id="a65d7-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="a65d7-119"><dt>**Nenhuma informação**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="a65d7-120">Posição do bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="a65d7-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="a65d7-121">Nenhuma informação é fornecida.</span><span class="sxs-lookup"><span data-stu-id="a65d7-121">No information is given.</span></span> <span data-ttu-id="a65d7-122">A referência do segredo é conhecida antes de emitir o comando ou é fornecida no campo de dados.</span><span class="sxs-lookup"><span data-stu-id="a65d7-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="a65d7-123"><dt>**Ref global**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="a65d7-124">Posição do bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="a65d7-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="a65d7-125">Dados de referência global (uma chave específica de MF).</span><span class="sxs-lookup"><span data-stu-id="a65d7-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="a65d7-126"><dt>**Referência específica**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="a65d7-127">Posição do bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="a65d7-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="a65d7-128">Dados de referência específicos (uma chave específica de DF).</span><span class="sxs-lookup"><span data-stu-id="a65d7-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="a65d7-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="a65d7-130">Posição do bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="a65d7-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="a65d7-131">00 (outros valores são RFU).</span><span class="sxs-lookup"><span data-stu-id="a65d7-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="a65d7-132"><dt>**RADIUS**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="a65d7-133">Posição do bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="a65d7-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="a65d7-134">Número do segredo.</span><span class="sxs-lookup"><span data-stu-id="a65d7-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="a65d7-135">*pChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65d7-136">Um ponteiro para os dados relacionados à autenticação.</span><span class="sxs-lookup"><span data-stu-id="a65d7-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="a65d7-137">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a65d7-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a65d7-138">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a65d7-139">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a65d7-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a65d7-140">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="a65d7-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a65d7-141">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="a65d7-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65d7-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a65d7-142">Return value</span></span>

<span data-ttu-id="a65d7-143">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a65d7-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a65d7-144">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a65d7-144">Return code</span></span>                                                                                   | <span data-ttu-id="a65d7-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="a65d7-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a65d7-146"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a65d7-147">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="a65d7-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a65d7-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a65d7-149">Um parâmetro inválido foi passado.</span><span class="sxs-lookup"><span data-stu-id="a65d7-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="a65d7-150"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a65d7-151">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="a65d7-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="a65d7-152"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a65d7-153">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="a65d7-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="a65d7-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="a65d7-154">Remarks</span></span>

<span data-ttu-id="a65d7-155">Para que o comando encapsulado seja bem-sucedido, o último desafio obtido do cartão deve ser válido.</span><span class="sxs-lookup"><span data-stu-id="a65d7-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="a65d7-156">As comparações malsucedidas podem ser registradas no cartão (por exemplo, para limitar o número de outras tentativas de uso dos dados de referência).</span><span class="sxs-lookup"><span data-stu-id="a65d7-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="a65d7-157">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a65d7-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a65d7-158">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a65d7-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a65d7-159">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a65d7-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a65d7-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a65d7-160">Requirements</span></span>



| <span data-ttu-id="a65d7-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65d7-161">Requirement</span></span> | <span data-ttu-id="a65d7-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a65d7-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65d7-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a65d7-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a65d7-164">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a65d7-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a65d7-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a65d7-166">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a65d7-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a65d7-167">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a65d7-167">End of client support</span></span><br/>    | <span data-ttu-id="a65d7-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a65d7-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a65d7-169">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a65d7-169">End of server support</span></span><br/>    | <span data-ttu-id="a65d7-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a65d7-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a65d7-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a65d7-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65d7-172"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a65d7-173">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a65d7-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="a65d7-174"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a65d7-175">DLL</span><span class="sxs-lookup"><span data-stu-id="a65d7-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65d7-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a65d7-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a65d7-177">IID</span><span class="sxs-lookup"><span data-stu-id="a65d7-177">IID</span></span><br/>                      | <span data-ttu-id="a65d7-178">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a65d7-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a65d7-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="a65d7-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65d7-180">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="a65d7-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="a65d7-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a65d7-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
