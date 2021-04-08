---
description: Constrói um comando APDU (unidade de dados de protocolo de aplicativo) que inicia a computação dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante (por exemplo, uma chave) armazenado no cartão.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'Método ISCardISO7816:: InternalAuthenticate (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010827"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="378ed-103">Método ISCardISO7816:: InternalAuthenticate</span><span class="sxs-lookup"><span data-stu-id="378ed-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="378ed-104">\[O método **InternalAuthenticate** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="378ed-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="378ed-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="378ed-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="378ed-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="378ed-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="378ed-107">O método **InternalAuthenticate** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que inicia a computação dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante (por exemplo, uma chave) armazenados no cartão.</span><span class="sxs-lookup"><span data-stu-id="378ed-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="378ed-108">Quando o segredo relevante é anexado ao MF, o comando pode ser usado para autenticar o cartão como um todo.</span><span class="sxs-lookup"><span data-stu-id="378ed-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="378ed-109">Quando o segredo relevante é anexado a outra DF, o comando pode ser usado para autenticar essa DF.</span><span class="sxs-lookup"><span data-stu-id="378ed-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="378ed-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="378ed-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="378ed-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="378ed-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="378ed-112">*byAlgorithmRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ed-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ed-113">Referência do algoritmo no cartão.</span><span class="sxs-lookup"><span data-stu-id="378ed-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="378ed-114">Se esse valor for zero, isso indica que nenhuma informação é fornecida.</span><span class="sxs-lookup"><span data-stu-id="378ed-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="378ed-115">A referência do algoritmo é conhecida antes de emitir o comando ou é fornecida no campo de dados.</span><span class="sxs-lookup"><span data-stu-id="378ed-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="378ed-116">*bySecretRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ed-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ed-117">Referência do segredo.</span><span class="sxs-lookup"><span data-stu-id="378ed-117">Reference of the secret.</span></span>



| <span data-ttu-id="378ed-118">Valor</span><span class="sxs-lookup"><span data-stu-id="378ed-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="378ed-119">Significado</span><span class="sxs-lookup"><span data-stu-id="378ed-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="378ed-120"><dt>**Nenhuma informação**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="378ed-121">Posição do bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="378ed-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="378ed-122">Nenhuma informação é fornecida.</span><span class="sxs-lookup"><span data-stu-id="378ed-122">No information is given.</span></span> <span data-ttu-id="378ed-123">A referência do segredo é conhecida antes de emitir o comando ou é fornecida no campo de dados.</span><span class="sxs-lookup"><span data-stu-id="378ed-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="378ed-124"><dt>**Ref global**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="378ed-125">Posição do bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="378ed-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="378ed-126">Dados de referência global (uma chave específica de MF).</span><span class="sxs-lookup"><span data-stu-id="378ed-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="378ed-127"><dt>**Referência específica**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="378ed-128">Posição do bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="378ed-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="378ed-129">Dados de referência específicos (uma chave específica de DF).</span><span class="sxs-lookup"><span data-stu-id="378ed-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="378ed-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="378ed-131">Posição do bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="378ed-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="378ed-132">00 (outros valores são RFU).</span><span class="sxs-lookup"><span data-stu-id="378ed-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="378ed-133"><dt>**RADIUS**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="378ed-134">Posição do bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="378ed-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="378ed-135">Número do segredo.</span><span class="sxs-lookup"><span data-stu-id="378ed-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="378ed-136">*pChallenge* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ed-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ed-137">Ponteiro para os dados relacionados à autenticação (por exemplo, desafio).</span><span class="sxs-lookup"><span data-stu-id="378ed-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="378ed-138">*lReplyBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="378ed-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="378ed-139">Número máximo de bytes esperados em resposta.</span><span class="sxs-lookup"><span data-stu-id="378ed-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="378ed-140">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="378ed-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="378ed-141">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="378ed-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="378ed-142">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="378ed-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="378ed-143">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="378ed-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="378ed-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="378ed-144">Return value</span></span>

<span data-ttu-id="378ed-145">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="378ed-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="378ed-146">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="378ed-146">Return code</span></span>                                                                                   | <span data-ttu-id="378ed-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="378ed-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="378ed-148"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="378ed-149">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="378ed-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="378ed-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="378ed-151">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="378ed-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="378ed-152"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="378ed-153">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="378ed-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="378ed-154"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="378ed-155">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="378ed-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="378ed-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="378ed-156">Remarks</span></span>

<span data-ttu-id="378ed-157">A execução bem-sucedida do comando pode estar sujeita a uma conclusão bem-sucedida de comandos anteriores (por exemplo, verificar ou Selecionar arquivo) ou seleções (por exemplo, o segredo relevante).</span><span class="sxs-lookup"><span data-stu-id="378ed-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="378ed-158">Se uma chave e um algoritmo estiverem selecionados no momento durante a emissão do comando, o comando poderá usar implicitamente a chave e o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="378ed-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="378ed-159">O número de vezes que o comando é emitido pode ser registrado no cartão para limitar o número de tentativas adicionais de usar o segredo relevante ou o algoritmo.</span><span class="sxs-lookup"><span data-stu-id="378ed-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="378ed-160">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="378ed-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="378ed-161">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="378ed-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="378ed-162">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="378ed-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="378ed-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="378ed-163">Requirements</span></span>



| <span data-ttu-id="378ed-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="378ed-164">Requirement</span></span> | <span data-ttu-id="378ed-165">Valor</span><span class="sxs-lookup"><span data-stu-id="378ed-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="378ed-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378ed-166">Minimum supported client</span></span><br/> | <span data-ttu-id="378ed-167">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="378ed-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="378ed-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="378ed-168">Minimum supported server</span></span><br/> | <span data-ttu-id="378ed-169">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="378ed-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="378ed-170">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="378ed-170">End of client support</span></span><br/>    | <span data-ttu-id="378ed-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="378ed-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="378ed-172">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="378ed-172">End of server support</span></span><br/>    | <span data-ttu-id="378ed-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="378ed-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="378ed-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="378ed-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="378ed-175"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="378ed-176">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="378ed-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="378ed-177"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="378ed-178">DLL</span><span class="sxs-lookup"><span data-stu-id="378ed-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="378ed-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="378ed-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="378ed-180">IID</span><span class="sxs-lookup"><span data-stu-id="378ed-180">IID</span></span><br/>                      | <span data-ttu-id="378ed-181">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="378ed-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="378ed-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="378ed-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="378ed-183">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="378ed-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="378ed-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="378ed-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
