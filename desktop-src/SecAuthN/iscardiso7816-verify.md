---
description: Constrói um comando APDU (unidade de dados do protocolo de aplicativo) que inicia a comparação (no cartão) dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão (por exemplo, senha).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'Método ISCardISO7816:: Verify (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752013"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="4666f-103">Método ISCardISO7816:: Verify</span><span class="sxs-lookup"><span data-stu-id="4666f-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="4666f-104">\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4666f-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4666f-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4666f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4666f-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4666f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4666f-107">O método **Verify** constrói um comando APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) que inicia a comparação (no cartão) dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão (por exemplo, senha).</span><span class="sxs-lookup"><span data-stu-id="4666f-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="4666f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4666f-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="4666f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4666f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4666f-110">*byRefCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4666f-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4666f-111">Um quantificador dos dados de referência.</span><span class="sxs-lookup"><span data-stu-id="4666f-111">A quantifier of the reference data.</span></span> <span data-ttu-id="4666f-112">A codificação do controle de referência P2 segue.</span><span class="sxs-lookup"><span data-stu-id="4666f-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="4666f-113">Quando o corpo estiver vazio, o comando poderá ser usado para recuperar o número ' X ' de novas tentativas permitidas (SW1-SW2 = 63CX) ou para verificar se a verificação não é necessária (SW1-SW2 = 9000).</span><span class="sxs-lookup"><span data-stu-id="4666f-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="4666f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4666f-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="4666f-115">Significado</span><span class="sxs-lookup"><span data-stu-id="4666f-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="4666f-116"><dt>**Nenhuma informação**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="4666f-117">Posição do bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="4666f-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="4666f-118">P2 = 00 é reservado para indicar que nenhum qualificador específico é usado nesses cartões em que o comando VERIFY referencia os dados secretos de forma inequívoca.</span><span class="sxs-lookup"><span data-stu-id="4666f-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="4666f-119"><dt>**Ref global**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="4666f-120">Posição do bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="4666f-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="4666f-121">Um exemplo de ref global seria uma senha.</span><span class="sxs-lookup"><span data-stu-id="4666f-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="4666f-122"><dt>**Referência específica**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="4666f-123">Posição do bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="4666f-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="4666f-124">Um exemplo de ref específica é uma senha específica de DF.</span><span class="sxs-lookup"><span data-stu-id="4666f-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="4666f-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="4666f-126">Posição do bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="4666f-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="4666f-127"><dt>**Dados de referência \#**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="4666f-128">Posição do bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="4666f-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="4666f-129">O número de dados de referência pode ser, por exemplo, um número de senha ou um identificador curto do EF.</span><span class="sxs-lookup"><span data-stu-id="4666f-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="4666f-130">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4666f-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4666f-131">Um ponteiro para os dados de verificação.</span><span class="sxs-lookup"><span data-stu-id="4666f-131">A pointer to the verification data.</span></span> <span data-ttu-id="4666f-132">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4666f-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="4666f-133">O valor padrão é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4666f-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4666f-134">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4666f-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4666f-135">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4666f-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="4666f-136">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="4666f-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="4666f-137">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="4666f-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4666f-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4666f-138">Return value</span></span>

<span data-ttu-id="4666f-139">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4666f-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4666f-140">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4666f-140">Return code</span></span>                                                                                   | <span data-ttu-id="4666f-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="4666f-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4666f-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4666f-143">A operação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4666f-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="4666f-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4666f-145">Um parâmetro que não é válido foi usado.</span><span class="sxs-lookup"><span data-stu-id="4666f-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="4666f-146"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4666f-147">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="4666f-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="4666f-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4666f-149">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4666f-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="4666f-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="4666f-150">Remarks</span></span>

<span data-ttu-id="4666f-151">O status de segurança pode ser modificado como resultado de uma comparação.</span><span class="sxs-lookup"><span data-stu-id="4666f-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="4666f-152">As comparações malsucedidas podem ser registradas no cartão (por exemplo, para limitar o número de outras tentativas de uso dos dados de referência).</span><span class="sxs-lookup"><span data-stu-id="4666f-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="4666f-153">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="4666f-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="4666f-154">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4666f-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4666f-155">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4666f-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4666f-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4666f-156">Requirements</span></span>



| <span data-ttu-id="4666f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="4666f-157">Requirement</span></span> | <span data-ttu-id="4666f-158">Valor</span><span class="sxs-lookup"><span data-stu-id="4666f-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4666f-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4666f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="4666f-160">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4666f-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4666f-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4666f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="4666f-162">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4666f-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4666f-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4666f-163">End of client support</span></span><br/>    | <span data-ttu-id="4666f-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4666f-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4666f-165">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4666f-165">End of server support</span></span><br/>    | <span data-ttu-id="4666f-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4666f-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4666f-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4666f-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="4666f-168"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4666f-169">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4666f-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="4666f-170"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4666f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4666f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4666f-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4666f-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4666f-173">IID</span><span class="sxs-lookup"><span data-stu-id="4666f-173">IID</span></span><br/>                      | <span data-ttu-id="4666f-174">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4666f-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="4666f-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="4666f-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4666f-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="4666f-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
