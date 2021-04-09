---
description: Constrói um comando APDU que inicia uma das operações listadas.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'Método ISCardISO7816:: WriteRecord (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089942"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="3333d-103">Método ISCardISO7816:: WriteRecord</span><span class="sxs-lookup"><span data-stu-id="3333d-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="3333d-104">\[O método **WriteRecord** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3333d-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3333d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3333d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3333d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3333d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3333d-107">O método **WriteRecord** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que inicia uma das seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="3333d-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="3333d-108">A gravação uma vez de um registro.</span><span class="sxs-lookup"><span data-stu-id="3333d-108">The write once of a record.</span></span>
-   <span data-ttu-id="3333d-109">Os bytes lógicos **ou** dos dados de um registro já presentes no cartão com os bytes de dados do registro fornecido no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="3333d-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="3333d-110">Os bytes lógicos e dos dados de um registro já presentes no cartão com os bytes de dados do registro fornecido no comando APDU.</span><span class="sxs-lookup"><span data-stu-id="3333d-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="3333d-111">Quando nenhuma indicação é fornecida no byte de codificação de dados, a lógica ou o comportamento se aplica.</span><span class="sxs-lookup"><span data-stu-id="3333d-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="3333d-112">Ao usar o endereçamento de registro atual, o comando define o ponteiro de registro no registro atualizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="3333d-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3333d-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3333d-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="3333d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3333d-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3333d-115">*byRecordId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333d-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333d-116">Identificação de registro.</span><span class="sxs-lookup"><span data-stu-id="3333d-116">Record identification.</span></span> <span data-ttu-id="3333d-117">Este é o valor P1:</span><span class="sxs-lookup"><span data-stu-id="3333d-117">This is the P1 value:</span></span>

<span data-ttu-id="3333d-118">P1 = ' 00 ' designa o registro atual.</span><span class="sxs-lookup"><span data-stu-id="3333d-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="3333d-119">P1! = ' 00 ' é o número do registro especificado.</span><span class="sxs-lookup"><span data-stu-id="3333d-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="3333d-120">*byRefCtrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333d-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333d-121">Codificação do controle de referência P2.</span><span class="sxs-lookup"><span data-stu-id="3333d-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="3333d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3333d-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="3333d-123">Significado</span><span class="sxs-lookup"><span data-stu-id="3333d-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="3333d-124"><dt>**EF atual**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="3333d-125">Posição do bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="3333d-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="3333d-126">EF selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="3333d-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="3333d-127"><dt>**ID curta do EF**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="3333d-128">Posição do bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="3333d-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="3333d-129">Identificador curto do EF.</span><span class="sxs-lookup"><span data-stu-id="3333d-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="3333d-130"><dt>**Primeiro registro**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="3333d-131">Posição do bit:-----000</span><span class="sxs-lookup"><span data-stu-id="3333d-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="3333d-132"><dt>**Último registro**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="3333d-133">Posição do bit:-----001</span><span class="sxs-lookup"><span data-stu-id="3333d-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="3333d-134"><dt>**Próximo registro**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="3333d-135">Posição do bit:-----010</span><span class="sxs-lookup"><span data-stu-id="3333d-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="3333d-136"><dt>**Registro anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="3333d-137">Posição do bit:-----011</span><span class="sxs-lookup"><span data-stu-id="3333d-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="3333d-138"><dt>**Registro \# em P1**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="3333d-139">Posição do bit:-----100</span><span class="sxs-lookup"><span data-stu-id="3333d-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="3333d-140">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333d-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333d-141">Ponteiro para o registro a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="3333d-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="3333d-142">*ppCmd* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3333d-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3333d-143">Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3333d-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="3333d-144">No retorno, ele é preenchido com o comando APDU construído por essa operação.</span><span class="sxs-lookup"><span data-stu-id="3333d-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="3333d-145">Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="3333d-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3333d-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3333d-146">Return value</span></span>

<span data-ttu-id="3333d-147">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3333d-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3333d-148">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3333d-148">Return code</span></span>                                                                                   | <span data-ttu-id="3333d-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="3333d-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3333d-150"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3333d-151">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3333d-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3333d-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3333d-153">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3333d-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3333d-154"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3333d-155">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="3333d-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3333d-156"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3333d-157">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3333d-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3333d-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="3333d-158">Remarks</span></span>

<span data-ttu-id="3333d-159">O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.</span><span class="sxs-lookup"><span data-stu-id="3333d-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="3333d-160">Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.</span><span class="sxs-lookup"><span data-stu-id="3333d-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="3333d-161">Se outro arquivo elementar estiver selecionado atualmente no momento da emissão desse comando, esse comando poderá ser processado sem a identificação do arquivo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="3333d-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="3333d-162">Se o comando encapsulado se aplicar a um arquivo elementar de forma linear ou fixada cíclica, ele será anulado se o tamanho do registro for diferente do tamanho do registro existente.</span><span class="sxs-lookup"><span data-stu-id="3333d-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="3333d-163">Se ele se aplicar a um arquivo elementar de variável linear, ele poderá ser executado quando o tamanho do registro for diferente do tamanho do registro existente.</span><span class="sxs-lookup"><span data-stu-id="3333d-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="3333d-164">Se P2 = xxxxx011 e o arquivo elementar for um arquivo cíclico, esse comando terá o mesmo comportamento que um comando construído usando [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="3333d-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="3333d-165">Os arquivos elementares sem uma estrutura de registro não podem ser gravados.</span><span class="sxs-lookup"><span data-stu-id="3333d-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="3333d-166">O comando construído é anulado se aplicado a um arquivo elementar sem uma estrutura de registro.</span><span class="sxs-lookup"><span data-stu-id="3333d-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="3333d-167">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="3333d-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="3333d-168">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3333d-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3333d-169">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3333d-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3333d-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3333d-170">Requirements</span></span>



| <span data-ttu-id="3333d-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="3333d-171">Requirement</span></span> | <span data-ttu-id="3333d-172">Valor</span><span class="sxs-lookup"><span data-stu-id="3333d-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3333d-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333d-173">Minimum supported client</span></span><br/> | <span data-ttu-id="3333d-174">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3333d-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3333d-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333d-175">Minimum supported server</span></span><br/> | <span data-ttu-id="3333d-176">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3333d-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3333d-177">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3333d-177">End of client support</span></span><br/>    | <span data-ttu-id="3333d-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3333d-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3333d-179">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3333d-179">End of server support</span></span><br/>    | <span data-ttu-id="3333d-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3333d-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3333d-181">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3333d-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="3333d-182"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3333d-183">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3333d-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="3333d-184"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3333d-185">DLL</span><span class="sxs-lookup"><span data-stu-id="3333d-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3333d-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3333d-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3333d-187">IID</span><span class="sxs-lookup"><span data-stu-id="3333d-187">IID</span></span><br/>                      | <span data-ttu-id="3333d-188">IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3333d-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3333d-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="3333d-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3333d-190">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="3333d-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="3333d-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="3333d-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="3333d-192">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="3333d-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="3333d-193">**Atualizarregistro**</span><span class="sxs-lookup"><span data-stu-id="3333d-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
